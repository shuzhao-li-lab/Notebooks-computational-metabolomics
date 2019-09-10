# Notebooks in Computational Metabolomics
Jupyter notebooks covering topics in metabolomics data analysis and computational methods. Free in the 3-Clause BSD License. Ongoing. Contributions are welcome.

## Use Jupyter notebooks via Docker containers

### Install Docker
Example on Linux (Ubuntu/Mint), instructed as -
https://docs.docker.com/install/linux/docker-ce/ubuntu/

`sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common`

`shuzhao@X3:~$  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`
OK

`shuzhao@X3:~$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"`
`shuzhao@X3:~$ sudo apt update`

`shuzhao@X3:~$ sudo apt-get install docker-ce docker-ce-cli containerd.io`

**Test Docker**
`shuzhao@X3:~$ sudo docker run hello-world`

**Add me to docker group, so I don't have to use sudo to run docker**
`shuzhao@X3:~$ sudo groupadd docker`
`shuzhao@X3:~$ sudo usermod -aG docker $USER`
`shuzhao@X3:~$ newgrp docker`


### Use data science stack via Docker
instructed as -
https://jupyter-docker-stacks.readthedocs.io/en/latest/

**Scipy notebook**
This also maps to local directory w/proj_test:

docker run -v /home/shuzhao/w/proj_test:/home/jovyan/p1 -p 8888:8888 jupyter/scipy-notebook

**R notebook**
docker run -v /home/shuzhao/w/proj_test:/home/jovyan/p1 -p 8888:8888 jupyter/r-notebook


## Example notebooks

- [Averaging technical replicates](notebooks/Averaging_technical_replicates.ipynb)

- [Statistical analyses of metabolite features (group comparison)](notebooks/Statistics_group_comparison.ipynb)

- [Clustering of metabolite peaks from LC-MS](notebooks/HCL_clustering_considering_retention_time.ipynb)

- [Bubble plot, using scatter plot panels to visualize result from pathway analysis](notebooks/Bubble_plot_pathways.ipynb)

## Additional notebooks:

- http://mummichog.org/notebooks.html
