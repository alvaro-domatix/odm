# Odoo development manager
pure bash docker-compose frontend for managing odoo development instances


## preface
- this will install an executable in `/usr/bin/` called `cnt`; before installing check that it doesn't conflict with your system configuration. regarding docker
a `domatix/odoo:base` image will be installed; you alse need to check that this does not conflict with your current system configuration.

- this document explains the basic installation and update steps. if you want to know the ins and outs for this program, check the dev documentation @ the [wiki](https://gitlab.domatix.com/catalin/odoo-dev/wikis/home)


## install
### dependencies
- gnu make
- docker 
- docker-compose
- expect

### installation

```bash
git clone https://gitlab.domatix.com/catalin/odoo-dev
cd odoo-dev
sudo make install # this will create the cnt executable
```





## update

if you updated the script from upstream, chances are that the utilities your containers have are not updated

```bash
cd your-odoo-dev-root-path
make update_conf
```
if you want to update only a specific container:
```bash
cp helper-scripts/* containers/<your-odoo-container>/custom/
```
