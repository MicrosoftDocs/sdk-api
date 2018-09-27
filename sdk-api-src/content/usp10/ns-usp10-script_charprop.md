---
UID: NS:usp10.script_charprop
title: script_charprop
author: windows-sdk-content
description: Contains information about a single character in a run (input string). The information indicates if the character glyph is affected by surrounding letters of the run.
old-location: intl\script_charprop.htm
tech.root: Intl
ms.assetid: 2f3a4d8d-c7b1-4005-aebb-d3e9f2e3a37f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SCRIPT_CHARPROP, SCRIPT_CHARPROP structure [Internationalization for Windows Applications], _win32_SCRIPT_CHARPROP, intl.script_charprop, script_charprop, usp10/SCRIPT_CHARPROP
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Usp10.h
api_name:
 - SCRIPT_CHARPROP
product: Windows
targetos: Windows
req.typenames: SCRIPT_CHARPROP
req.redist: Usp10.dll version 1.600 or greater onWindows XP
---

# script_charprop structure


## -description



Contains information about a single character in a run (input string). The information indicates if the character glyph is affected by surrounding letters of the run.




## -struct-fields




### -field fCanGlyphAlone

Value indicating if the shaping of a letter depends on other characters around the letter being shaped. Possible values are defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>TRUE</td>
<td>The shape of a letter is independent of surrounding characters.</td>
</tr>
<tr>
<td>FALSE</td>
<td>The shape of a letter depends on one or more adjacent characters.</td>
</tr>
</table>
 


### -field reserved

Reserved.


## -remarks



One or more characters in a run, immediately preceding and/or following the letter being shaped, can influence shaping. Information about these characters can help optimize higher-level layout code, such as that used to optimize paragraph layout.


#### Examples

Let's look at an example of the use of this structure.



<ul>
<li>A font has ligatures for letter combinations "fi" and "fl", and no others. 
</li>
<li>The input string is "I like flying fish".</li>
<li> 
An array of <b>SCRIPT_CHARPROP</b> structures contains one structure for each character of the input string. 
</li>
</ul>
For the provided input string, the array of structures has the following values in the <b>fCanGlyphAlone</b> members:


```cpp
I like flying fish
111111100111110011

```





## -see-also




<a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a>



<a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

