drone-cc
========

`drone-cc` is a simple CCMenu component for the [Drone CI server](https://github.com/drone/drone).

## Clients

* [CCMenu](http://ccmenu.org/) (Mac)
* [buildnotify](https://bitbucket.org/Anay/buildnotify/wiki/Home) (Unix)
* [CCTray](http://cruisecontrolnet.org/projects/ccnet/wiki/CCTray_Download_Plugin) (Windows)

## XML API

Caveat: These were reversed-engineered from some TravisCI repos' output. I didn't bother to look for official XML spec, I'm sure there's tons of other statuses not represented. I just wanted pass/fail/building.

### During Building

    <Projects>
      <Project
        name="freesurface/mom"
        activity="Building"
        lastBuildStatus="Unknown"
        lastBuildLabel="89"
        lastBuildTime=""
        webUrl="https://travis-ci.org/freesurface/mom" />
    </Projects>


### Succeeded

    <Projects>
      <Project
        name="freesurface/mom"
        activity="Sleeping"
        lastBuildStatus="Success"
        lastBuildLabel="89"
        lastBuildTime="2014-05-02T20:36:55.000+0000"
        webUrl="https://travis-ci.org/freesurface/mom" />
    </Projects>
