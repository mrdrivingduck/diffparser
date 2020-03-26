# diffparser

⛏️ Parse unified diffs with Java.

Created by : [@thombergs](https://github.com/thombergs)

Modified by : Mr Dk.

2020 / 03 / 27 02:02

Ningbo, Zhejiang, China

---

## Code example

```java
DiffParser parser = new UnifiedDiffParser();
InputStream in = new FileInputStream("/path/to/file.diff");
List<Diff> diff = parser.parse(in);
```

## What Diff formats can be parsed?

Currently, the only implementation of the DiffParser interface is UnifiedDiffParser, which supports parsing of diffs like the following:

```diff
Modified: trunk/test1.txt
===================================================================
--- /trunk/test1.txt	2013-10-23 19:41:56 UTC (rev 46)
+++ /trunk/test1.txt	2013-10-23 19:44:39 UTC (rev 47)
@@ -1,4 +1,3 @@
 test1
-test1
+test234

-test1
\ No newline at end of file
@@ -5,9 +6,10 @@
-test1
-test1
+aösdhasd
+asdasd
```

An input stream may contain several sections like the above, delimited by an empty line. Each such section will be parsed into an object
of class Diff.

## Latest Stable Release

In [release](https://github.com/mrdrivingduck/diffparser/releases).

---

