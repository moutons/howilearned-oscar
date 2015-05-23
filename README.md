## How I Learned to Stop Worrying and Love the ENC

Vagrant, Oscar, single Master and Agent nodes, what? 

[Read the slides](http://slides.com/moutons/oscar-strangelove#/) if you want to.

To get set up with a quick Vagrant + Oscar + r10k [@glarizza style](http://garylarizza.com/) setup, clone the repo to a handy directory, run `./getready` then run `vagrant up master`, once that's done provisioning run `vagrant up`. I know I should explain more about the process, and I'll try to get to that at some point.

Turns out, I should have tested better. My script worked fine on an older system but appears to fail on Ubuntu 15.04, so here are some steps to get things working:

1. Install [Vagrant](https://vagrantup.com)
1. Install [Virtualbox](https://virtualbox.org)
1. Run the following commands:

```shell
vagrant plugin install oscar
vagrant plugin install vagrant-auto_network
vagrant plugin install vagrant-hosts
vagrant box add puppetlabs/centos-6.6-64-nocm --provider=virtualbox
mkdir -p ./git
git clone https://github.com/moutons/howilearned-control.git ./git/howilearned-control
git clone https://github.com/moutons/howilearned-hiera.git ./git/howilearned-hiera
```
That should get you ready to go, I think.

To use it, you should be able to just run `vagrant up`.

Let me know if it doesn't work?

```
         _n_
         \O
     ____,/)____
   ,'  |  <   | \<
   `.__|______|_/<  SSt
```

### Bears

![what are they up to](http://i.imgur.com/M8FUl.jpg)

* you know, like a BEAR repository? a BARE repository?

![no seriously what are they up to](http://i.imgur.com/3jxqrKP.jpg)

