# halogenOS
## Official devices application

Before you apply to add your device into our list of official devices, you should know a few things:

Any failure in following the below instructions will make you unfit for the maintainership. No questions asked.

### 1. To turn into a maintainer of halogenOS:

1.2 - You must own the device. Blind and untested builds aren't allowed.

1.3 - You must have knowledge of git, bash and basic building.

1.4 - You must do an unofficial build for at least 2 weeks, be sure that the build is stable for daily usage before applying.
      Stability context may differ for different devices, so explain for any exceptions.

1.5 - You must have your device sources public and up-to-date. Any release must have all source code publicly available in such a way
      that anyone can build it.

### 2. Maintainers conduct notes:

2.2 - The maintainers mustn't do any unofficial modifications. Local changes have to be pushed.
      Also, a maintainer mustn't send an update to users with unmerged gerrit changes.

2.3 - The maintainers must arrange repository creation and permission grantin on gerrit with the project leaders. The trees should fully reflect the changes when a new build is pushed for that specific device tree. Last but not the least, it should be fully buildable as mentioned above.

2.4 - The maintainers must test or have a trusted person test every build before sending OTA update to user.

2.5 - The maintainers must keep authorship of git commits that are pushed, mandatory for all repositories.
      Commit messages have to be meaningful and describe the actual changes.
      If we find that a repository has too many undocumented non-trivial changes made by the maintainer we will reject the maintainership request
      until correction.

2.6 - Relationships fights can be done in PM on Telegram or XDA.

2.7 - The maintainers mustn't:

2.7.1 - Add any changes to the ROM base but are allowed to add device-specific changes to their device-specific repositories only.

2.8 - The maintainers are welcome to:

2.8.1 - Add improvements/bugfixes/features to their kernel/device tree as long as they do not affect stability, usability and user experience negatively

2.8.2 - Submit patches to our [Gerrit](https://review.halogenos.org)

2.8.3 - Merge kernel upstream into their kernel tree if it's done properly

2.9 - We allow our maintainers to:

2.9.1 - Use a custom toolchain as long as it does not affect, remove or interfere with existing toolchains

2.9.2 - Set SELinux to permissive for obsolete/older devices that are required to do so

2.9.3 - Create private testing groups on their preferred messaging platform (e. g. Telegram).

2.9.4 - Upload testing builds publicly as long as they are clearly marked as such and not posted on any public website, channel or group
        (you can share it in your private testing group)

### 3. Building and hosting

Building is done by one of the project members or trusted maintainers.
The builds are automatically uploaded to our GitHub release page.

### 4. Changelog
For each new version, you need to upload the changelog to this repository in the device specific folder.
To do so, submit a patch to our Gerrit.

The changelog file name must match the **.zip** file name and should end with **.txt**

Eg: **.zip** is **halogenOS_potter-9.0.0-20190714-0418-OFFICIAL.zip**, changelog file name should be **hhalogenOS_potter-9.0.0-20190714-0418-OFFICIAL.txt**

Maintainers should always try to write a user understandable changelog.

### 5. Over-the-air (OTA) updates

We do not support OTA updates yet.

### 6. JSON params

##### devices.json
| Param | Description | Required |
|--|--|--|
| name | Device name | Yes |
| brand | Device manufacturer | Yes |
| codename | Device codename, eg: falcon | Yes |
| version_code | Version code, lowercase, eg: pie | Yes |
| version_name | Version name, will be shown on download portal, eg: Pie | Yes |
| maintainer_name | Your name | Yes |
| maintainer_url | Your personal URL, eg: https://github.com/jhenrique09/ or https://forum.xda-developers.com/member.php?u=6519039 | No  |
| xda_thread | XDA thread URL, eg: https://forum.xda-developers.com/g5-plus/development/rom-pixel-experience-t3704064 | No |

##### builds/your_device_codename.json
| Param | Description | Required |
|--|--|--|
| file_name | Build file (.zip) name | Yes |
| file_size | Build file (.zip) size (in bytes) | Yes |
| md5 | Build file (.zip) md5 hash | Yes |

If you agree with everything, contact a project member.
