---
title: Content Plugin - Obix Content Restriction 
layout: post
author: pieter
permalink: /content-plugin---obix-content-restriction-/
source-id: 1gBp2CqFs9F-BhkmPuKWJZ1ClzwpsQJjpPE2eEmm126E
published: true
---
Content Plugin - Obix Content Restriction 

[[TOC]]

# Permission categories

**guest**

Content is not/only visible for guests, i.e. none registered users.

**user**

Content is not/only visible for specific users.

**user group**

Content is not/only visible for users that in specific groups.

**author**

Content is not/only visible for the user that created the article.

**featured article**

Content is only visible if the article it belongs to is displayed as a featured article.

**home page**

Content is only visible if the article it belongs to is displayed on the home page.

**language**

Content is only visible if the article is in a specific language.

**request**

Content is only visible if the url contains request variables with specific values.

# Logic

## Condition

expression

expression1 && expression2

expression1 || expression2

expression1 && (expression2 || expression3)

(expression1 && expression2) || (expression3 && expression4)

etc.

## Expression

variable

true or false

!variable

not true or false

variable=value

variable matches value

variable!=value

variable does not match value

variable=value2,value3,…,valueN

variable matches at least one of the listed values

# Syntax

**{restricted** **_condition_****}**restricted content**{otherwise}**non restricted content**{/restricted}**

* 'White space after ‘{‘ and before ‘}' is not allowed.

## Variables

### guest

{restricted guest}...{/restricted}

### user

{restricted user[!]=id1[,id2,id3,...,idN]}...{/restricted}

### usergroup

{restricted usergroup[!]=id1[,id2,id3,...,idN]}...{/restricted}

### viewlevel

{restricted viewlevel[!]=id1[,id2,id3,...,idN]}...{/restricted}

### author

{restricted author}...{/restricted}

### featured

{restricted featured}...{/restricted}

### homepage

{restricted homepage}...{/restricted}

### language

{restricted language[!]=id1[,id2,id3,...,idN]}...{/restricted}

### request

{restricted request[!]=var1:value1[,var2:value2, var3:value3,...,varN:valueN]...{/restricted}

