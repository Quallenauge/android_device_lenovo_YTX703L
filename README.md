Nothing to see here
===================

This repository exists for the sole purpose of satisfying the
`vendor/{cm,lineage}/build/tools/roomservice.py` script's need to
find a valid repository under `github.com/LineageOS/android_device_*_${device}`
that it can download (where ${device} is deduced from the lunch target,
say `lineage_${device}-userdebug`).

Until this `roomservice.py` limitation is removed, this repository needs
to continue to exist. See the following proposed changes on the review board
for more information:

* https://review.lineageos.org/c/LineageOS/android_vendor_cm/+/214013
* https://review.lineageos.org/c/LineageOS/android_vendor_cm/+/214014
* https://review.lineageos.org/c/LineageOS/android_vendor_cm/+/214032
* https://review.lineageos.org/c/LineageOS/hudson/+/214015/1

All product makefiles for LineageOS on the entirety of the Lenovo Yoga Tab 3
Plus family can be found inside the `android_device_lenovo_YTX703-common`
repository, under this same account. The only file in this repository
(other than the README) takes care to ensure that `roomservice.py` will
pick up the common device repository.

Having multiple product makefiles under the same repository in LineageOS
is possible under the constraints and limitations discussed below:

* https://review.lineageos.org/c/LineageOS/android_build/+/208737
* https://review.lineageos.org/c/LineageOS/android_build/+/208857/1
* https://review.lineageos.org/c/LineageOS/android_build/+/208856/1

You do not need to pick this repository if you are constructing your
`.repo/local_manifests/roomservice.xml` by hand.
