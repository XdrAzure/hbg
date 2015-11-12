# Habbo Badge Generator

This repository contains the necessary files to generate all badges from Habbo.
Requires PHP 7.0 or higher.

### IIS - Url Rewrite 2

```
<rule name="HBG-Xdr">
	<match url="^habbo-imaging/badge/(.*)" ignoreCase="false" />
	<conditions logicalGrouping="MatchAll" trackAllCaptures="false" />
	<action type="Rewrite" url="habbo-imaging/badge.php?badge={R:1}" />
</rule>
```

### Apache - mod_rewrite.c

```
RewriteRule ^habbo-imaging/badge/(.*) habbo-imaging/badge.php?badge=$1
```
