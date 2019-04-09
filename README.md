## Forked from soehest repo (unmaintained as of 2017) to be compatible with an up to date system primarily for my own use, but feel free to experiment ##

I found that many of the ebuilds from soehest overlay merely required some updates to be functional again, and I prefer to use ebuilds over building from source when I can.


# Experimental Gentoo Linux Ebuilds #

This Git repository contains experimental ebuilds for [Gentoo Linux](http://www.gentoo.org/). At this time it consists of the following ebuilds

- [sabnzbd](http://sabnzbd.org/)
- ~~[yenc](http://www.golug.it/yenc.html)~~ (Using portage now)
- [couchpotato](http://couchpota.to/)
- [sickbeard](http://sickbeard.com/)
- [headphones](https://github.com/rembo10/headphones)
- [maraschino](https://github.com/mrkipling/maraschino.git)
- ~~[libcec](http://libcec.pulse-eight.com/)~~ (Using portage now)
- [spotweb](https://github.com/spotweb/spotweb)
- [moviegrabber](http://sourceforge.net/projects/moviegrabber/)

sabnzbd and yenc has been forked from the [sunrise](http://overlays.gentoo.org/proj/sunrise) overlay and are both created by Sébastien P.

These ebuilds are also located in the Gentoo overlay soehest. To use the overlay type the following commands

```bash
emerge git layman
echo "source /var/lib/layman/make.conf" >> /etc/make.conf
layman -f
layman -a soehest
```

To update the overlay use the following command
```
layman -S
```

More info on Gentoo Layman can be found [here](http://www.gentoo.org/proj/en/overlays/userguide.xml)

To install one of the ebuilds from this overlay you need to add it to /etc/portage/package.keyword  

```ruby
echo "net-nntp/sabnzbd" >> /etc/portage/package.keywords
echo "net-nntp/yenc" >> /etc/portage/package.keywords
emerge sabnzbd
```

I take no responsibility if usage of these ebuilds makes your computer burn, crash, or start downloading naughty movies or country music. These builds are higly experimental. What works for me may not work for you. Now you have been warned!

As mentioned sabnzbd has been forked and quite some changes have been made. I decided to fork it as the sunrise overlay seemed to be stalled/unmaintained. ~~After this fork the original maintainer came to life and has agreed to maintain his build so hopefully it will go live into portage soon.~~
Frankly I do not see this happening anytime soon. As feedback is not overwhelming I am currently not considering adding this to portage.
