OSG Software Stack -- Data Release -- 3.4.5-2
==============================================

**Release Date**: 2017-11-20

Summary of changes
------------------

This release contains:

-   [VO Package v76](https://github.com/opensciencegrid/osg-vo-config/releases/tag/release-76)
    -   Drop redundant geant4-lcgadmin objects
    -   Add missing SNO+ VOMS servers
    -   Add notice to voms-mapfile-default

These [JIRA tickets](https://jira.opensciencegrid.org/issues/?jql=project%20%3D%20SOFTWARE%20AND%20fixVersion%20%3D%203.4.5-2%20ORDER%20BY%20priority%20DESC%2C%20key%20DESC) were addressed in this release.

Detailed changes are below. All of the documentation can be found [here](../../index.md)

Updating to the new release
---------------------------

### Update Repositories

To update to this series, you need to [install the current OSG repositories](../../common/yum.md#install-the-osg-repositories).

### Update Software

Once the repositories are installed, you can update to this new release with:

``` console
root@host # yum update
```

!!! note "Notes"
    -   Please be aware that running `yum update` may also update other RPMs. You can exclude packages from being updated using the `--exclude=[package-name or glob]` option for the `yum` command.
    -   Watch the yum update carefully for any messages about a `.rpmnew` file being created. That means that a configuration file had been edited, and a new default version was to be installed. In that case, RPM does not overwrite the edited configuration file but instead installs the new version with a `.rpmnew` extension. You will need to merge any edits that have made into the `.rpmnew` file and then move the merged version into place (that is, without the `.rpmnew` extension).

Need help?
----------

Do you need help with this release? [Contact us for help](../../common/help.md).

Detailed changes in this release
--------------------------------

### Packages

We added or updated the following packages to the production OSG yum repository. Note that in some cases, there are multiple RPMs for each package. You can click on any given package to see the set of RPMs or see the complete list below.

#### Enterprise Linux 6

-   [vo-client-76-1.osg34.el6](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=vo-client-76-1.osg34.el6)

#### Enterprise Linux 7

-   [vo-client-76-1.osg34.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=vo-client-76-1.osg34.el7)

### RPMs

If you wish to manually update your system, you can run yum update against the following packages:

    osg-gums-config vo-client vo-client-edgmkgridmap vo-client-lcmaps-voms

If you wish to only update the RPMs that changed, the set of RPMs is:

#### Enterprise Linux 6

``` file
osg-gums-config-76-1.osg34.el6
vo-client-76-1.osg34.el6
vo-client-edgmkgridmap-76-1.osg34.el6
vo-client-lcmaps-voms-76-1.osg34.el6
```

#### Enterprise Linux 7

``` file
osg-gums-config-76-1.osg34.el7
vo-client-76-1.osg34.el7
vo-client-edgmkgridmap-76-1.osg34.el7
vo-client-lcmaps-voms-76-1.osg34.el7
```

