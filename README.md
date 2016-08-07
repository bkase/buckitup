# Buck it up

Playing with facebook/buck#810 in an Android app.

## What I'm trying to do

To simulate a developer who wants to speed up the build for his or her app. 

Thus, I'm not using the `buck` skeletons -- I've created a "BlankActivity" project with Android Studio and ran the "Code > Convert Java File to Kotlin File" command on the auto-generated `MainActivity.java` from the wizard.

From here I'm trying to get Buck (from the facebook/buck#810 pull) to work

Once this trivial Hello World app builds, I'll buckify and depend on mathcamp/cheatsheet and mathcamp/fiberglass (two kotlin libraries I've built)

## Notes

* It's still quite difficult to set up buck from an Android Studio gradle project (I had no luck with OkBuilds/OkBuck ) -- zserge/buckbone was helpful (the Java skeleton since we want native Kotlin)
* I hit a snag trying to replace `android_library` with `kotlin_library` since we need the `android_library` support to build `MainActivity`.
* The `android_resource` rule has errors, but that's probably an easy fix
