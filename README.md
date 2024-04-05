# learning-woodpecker
Using [Woodpecker CI](https://woodpecker-ci.org/) self-hosted with [Codeberg](https://codeberg.org/) self-hosted runner.  

# runner
https://forgejo.org/docs/next/admin/actions/#forgejo-runner  

Forgejo give almost everything that you need  
```
wget -O forgejo-runner https://code.forgejo.org/forgejo/runner/releases/download/v3.3.0/forgejo-runner-3.3.0-linux-amd64
chmod +x forgejo-runner
wget -O forgejo-runner.asc https://code.forgejo.org/forgejo/runner/releases/download/v3.3.0/forgejo-runner-3.3.0-linux-amd64.asc
gpg --keyserver keys.openpgp.org --recv EB114F5E6C0DC2BCDD183550A4B61A2DC5923710
gpg --verify forgejo-runner.asc forgejo-runner
```

But doesn't tell you that you need to register too  
```
./forgejo-runner register
```

**Forgejo instance URL**: https://codeberg.org  
**Runner token**: Get at your organization "Settings > Actions > Runners"  
The rest is up to you to fill or not.  

Start runner with  
```
sudo ./forgejo-runner daemon
```
