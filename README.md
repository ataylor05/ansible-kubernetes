# Binance-Scalper
This was written to provide an on-prem installation of Kubernetes.

<br><br>
![Scalp1](images/scalp1.jpg?raw=true "Scalp1")


# Getting Started
Clone project or download the zip file.  Once the Binance-Scalper.py file is on your disk, run it as follows:<br>
```
python .\Binance-Scalper.py
```

# Commands
**Get cluster join tokens**
<pre>
Worker join token:
kubeadm token create --print-join-command

Control Plane join token:
kubeadm init phase upload-certs --upload-certs
kubeadm token create --print-join-command --certificate-key string
</pre>
<br>

**Remove a node.**
<pre>
kubectl drain <node name> --delete-local-data --force --ignore-daemonsets
kubeadm reset
kubectl delete node <node name>
</pre>