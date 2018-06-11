# Archey X

> Archey X is a simple tool to display system information.

![][masterBadge] [![GitHub release][latestBadge]][latest]

![][pythonVersion]

This is a forked/ported version of the original script: [Archey][dja], by [djmelek][djm] - made to be X compatible with both OS X and misc GNU/Linux distributions - hence the name: Archey **X**. _(Previously an OS X port of Archey.)_ […»][about]


### Screenshots

Here's a small demo you can watch at Vimeo.

[![][vimeo_poster]][vimeo]


v0.7.0-beta on OS X. (Terminal theme: [myTerm][myterm].)

![][scrap]


v0.X-beta _(early version)_ of Fedora and Debian in Vagrant boxes.

![][x2]

_A few more Screenshots can be found in the [Wiki …»][scraps]._


## Installation

Copy the file to `/usr/local/bin`, and give it permission to execute.

```bash
sudo install -v -m 0755 archeyX /usr/local/bin
```

_(make sure `/usr/local/bin` is in your `PATH`)_


## Usage

    archeyX

To load at start. Add to your `.bashrc` _(or `.bash_profile`)_:

```bash
# Load archeyX (if installed)
[[ `type archeyX 2> /dev/null` && $UID != 0 ]] && archeyX
```

> **Note:** When using `scp` over the network and logging into a machine with `archeyX` loading up... It _might_ cause an error about output. It's about being interactive or not. You can try/use one of these to surround it with:

> ```bash
> [ -z $PS1 ]
> [ -v $PS1 ]  # bash 4.2+
> [ -t 1 ]
> [[ $- =~ i ]]
> [[ $- == *i* ]]
> ```


## Settings and Colors

See [Settings and Colors][prefs] in the Wiki


## Tested distros

- [ ] Arch Linux
- [x] Darwin/OS X
- [x] Debian Jessie 8.3 (“may” work with other, like Mint, *buntu. `dpkg`)
- [x] Fedora 23 (“may” work with CentOS and Red Hat. `dnf|yum`)

_Please, report working distributions [here][iss1]._


## License, credits and copyright

![][licenseBadge]

See [Credits][credits] in the Wiki…


## Contributing

1. Fork it (<https://gitlab.com/iEFdev/Archey-X/forks/new>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Merge Request


## Author notes

-	**[2017-04-30]** From now, Arxhey X is using Python 3.6+. The “shebang” is changed, and there's a `f'{}'` to trigger an error with a msg to ask you to upgrade if you don't have 3.6. So, please upgrade if needed. Thanks!
-	**[2016-11-23]** This repo has been renamed from: “Archey :: OS X” -> “Archey X”, since it will be X-compatible. Initial version(s) will be `v0.7.0-YYYYMMDD-beta` until it's been tested/verified more to work with _N_ distributions.

**Pylint**

-	**[2017-05-01]** 9.96/10 (pylint 1.7.1, Python 3.6.1).


If you have any feedback, suggestions? Please, use the Issues, Pull requests, send an email or a tweet.

· Eric ([@iEFdev][twitter])

<!-- Markdown: link & image dfn's -->
[pythonVersion]: https://img.shields.io/badge/Python-%3E%3D_3.6-FAC826.svg?style=plastic&colorA=3D75AD&logoWidth=14
[licenseBadge]: https://img.shields.io/badge/license-GPL--3.0-orange.svg?style=plastic
[masterBadge]: https://img.shields.io/badge/master-v0.8--beta-778899.svg?style=plastic
[latestBadge]: https://img.shields.io/badge/latest-v0.7.0-blue.svg?style=plastic
[latest]: https://gitlab.com/iEFdev/Archey-X/tags/ "Tags"
[dja]: https://github.com/djmelik/archey "Archey"
[djm]: https://github.com/djmelik "Melik Manukyan"
[vimeo]: https://vimeo.com/217440806 "Archey X (demo)"
[vimeo_poster]: https://gitlab.com/iEFdev/Archey-X/raw/master/images/vimeo_poster.png "Archey X (demo)"
[scrap]: https://gitlab.com/iEFdev/Archey-X/raw/master/images/screenshot.png "Screenshot of Archey X"
[scraps]: https://gitlab.com/iEFdev/Archey-X/wikis/Screenshots "More Screenshots"
[x2]: https://gitlab.com/iEFdev/Archey-X/wikis/_Images/screenshot_x2.png "Screenshot(s) of Archey X"
[myterm]: https://gitlab.com/iEFdev/myTerm "My Terminal theme"
[about]: https://gitlab.com/iEFdev/Archey-X/wikis/About "About Archey X"
[credits]: https://gitlab.com/iEFdev/Archey-X/wikis/Credits "Credits and copyright"
[prefs]: https://gitlab.com/iEFdev/Archey-X/wikis/Settings-and-Colors "Settings and Colors"
[iss1]: https://gitlab.com/iEFdev/Archey-X/issues/1 "#1 - Verify distributions"
[twitter]: https://twitter.com/iEFdev
