# <a href="https://github.com/dmarcoux/znc">dmarcoux/znc</a>

My setup to run ZNC on *openSUSE Leap 15.0* hosted on *Hetzner*

### Setup

*openSUSE* is supported, but not as part of one of the official images. To install
*openSUSE* on a *Hetzner* server,

1. Deploy a *Hetzner* server with any of the official images using the web
   interface
2. Go under the `ISO Images` on the server's page
3. Mount the `openSUSE Leap 15.0` ISO image
4. Reboot the server
5. Install `openSUSE Leap 15.0`
6. Unmount the ISO image
7. Copy SSH public key to the server
   ```
   ssh-copy-id user@server_ip
   ```
7. SSH into the server
   ```
   ssh user@server_ip
   ```
8. Download the [initialization script](openSUSE-Leap-15.0.sh) to the server
   ```
   curl https://raw.githubusercontent.com/dmarcoux/znc/master/openSUSE-Leap-15.0.sh --output init.sh
   ```
9. Run the [initialization script](openSUSE-Leap-15.0.sh)
   ```
   bash init.sh
   ```

### TODOs

- [Terraform](https://www.terraform.io/docs/providers/hcloud/index.html)
- Domain
- Let's Encrypt certificate for the ZNC webadmin
