# Instructions

Just paste one of these two URLs into **Docker Repositories** on the **Docker**
tab:

~~~
https://code.nephatrine.net/NephNET/unraid-containers
https://github.com/nephatrine/unraid-containers
~~~

You should be able to find the templates when you add a new container.

## unRAID 6.10+

I went to check what URLs I had set as repositories and was at a loss because I
was unable to even find the area where you enter these anymore. If you had
already added the repo at some point in the past it will continue to work, but
adding it to a fresh installation is now a huge pain in the buttocks thanks to
unRAID deciding "no one used it" and removing this functionality.

The "officially supported" way to do this now is to add these as "applications"
in the Community Apps repository. I do *NOT* plan on doing this as it requires
maintaining a separate support thread on the unRAID forums and I only provide
support in my Gitea/Github repositories.

Here is Squid's "helpful" post on the topic from the unraid forums:

```
Beginning with Unraid 6.10.0-rc1, the entire Template Repositories section has been removed (Thanks be to JoBu)

2 Choices:

  1. save the xml's within /config/plugins/dockerMan/templates-user on the flash drive and use the Add Container Button
  2. save the xml's within /config/plugins/community.applications/private/nephatrine on the flash drive and use CA to manage them (If not categorized, they will appear within the Private Category)
```

I believe there may be a third option, but I don't have a fresh unRAID install to test with:

```bash
echo 'https://code.nephatrine.net/NephNET/unraid-containers' >>/config/plugins/dockerMan/template-repos
```
