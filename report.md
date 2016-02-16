A3 GFB 
Checking in 
Bug 1064821 - Throw Component.exceptions instead of strings in contentprefs
https://bugzilla.mozilla.org/show_bug.cgi?id=1064821

This bug is a fix of the source code in toolkit > contentprefs.
https://dxr.mozilla.org/mozilla-central/search?q=throw+path%3Atoolkit%2Fcomponents%2Fcontentprefs&case=true
The case is that exceptions are thrown as strings (since JS has no restriction on throws) however they should be appropriate exception objects.

I will read the source file to find these throw cases and replace them with excpetion objects accordingly (as described in the first comment on the bug page).

This can be tested by running code that will reach an exception case or by visually reviewing the exception cases in the code.

Screenshots will be provided.

