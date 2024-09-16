# ts-in-minikube



Welcome Tailscalers!

## Outline
- Create a personal Tailnet
- Deploy subnet router
- Add Tailscale device with SSH enabled 

### Environment:

- local minikube cluster installed on laptop
- create a subnet on laptop 
- enabled Trailscale on minikube with SSH

### Process for Laptop

1. Install [minikube](https://minikube.sigs.k8s.io/docs/start/?arch=%2Fmacos%2Fx86-64%2Fstable%2Fhomebrew) 
2. [Download and install Tailnet](https://tailscale.com/download)
```
I downloeaded Tailscale app to my laptop and my phone and successfully connected on my Tailnet. 
```
3. Enable subnet router
```
I configured IP forwarding on my laptop for Tailscale and the configured the advertise-routes parameter using the set command in CLI for Tailscale. 
```
4. Approve subnet in Tailscale Admin console
```
Since I don't have automatic approval for subnets, I navigated to my admin console to approve the routes. 
```
5. Test that subroutes are accessible
```
I was able to connect from a VM where I did not install Tailscale and I was able to successfully ping the laptop using the Tailscale IP address while inside the VM. 
```


### Process for minikube VM 

1. [Download and install Tailnet for Ubuntu Jammy - my minikiube VM](https://tailscale.com/kb/1187/install-ubuntu-2204)
2. [Configure Tailscale for SSH](https://tailscale.com/kb/1308/quick-guide-ssh-linux-vm)
```
After I successfully downloaded and installed Tailscale on the minikube VM, I was able to ping the VM from my laptop using the TailScale IP address of the minikube VM. Then I enabled SSH through the minikube VM Tailscale configuration and I was able to SSH into the minikube VM by using `SSH root@<tailscale-ip-address>` command in my terminal or the SSH button in my Tailscale admin console.
```

### Process for nginx pods 
**WIP** 


