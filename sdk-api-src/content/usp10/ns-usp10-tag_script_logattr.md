---
UID: NS:usp10.tag_SCRIPT_LOGATTR
title: tag_SCRIPT_LOGATTR
author: windows-sdk-content
description: Contains attributes of logical characters that are useful when editing and formatting text.
old-location: intl\script_logattr.htm
tech.root: Intl
ms.assetid: 24131b04-870a-4841-b9cd-7a09497bd2e6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FALSE, SCRIPT_LOGATTR, SCRIPT_LOGATTR structure [Internationalization for Windows Applications], TRUE, _win32_SCRIPT_LOGATTR_str, intl.script_logattr, tag_SCRIPT_LOGATTR, usp10/SCRIPT_LOGATTR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: usp10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - SCRIPT_LOGATTR
product: Windows
targetos: Windows
req.typenames: SCRIPT_LOGATTR
req.redist: Internet Explorer 5 or later onWindows Me/98/95
---

# tag_SCRIPT_LOGATTR structure


## -description



Contains attributes of logical characters that are useful when editing and formatting text.




## -struct-fields




### -field fSoftBreak

Value indicating if breaking the line in front of the character, called a "soft break", is valid. Possible values are defined in the following table. This member is set on the first character of Southeast Asian words.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
A soft break is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
A soft break is not valid.

</td>
</tr>
</table>
 


### -field fWhiteSpace

Value indicating if the character is one of the many Unicode characters classified as breakable white space. Possible values are defined in the following table. Breakable white space can break a word. All white space is breakable except nonbreaking space (NBSP) and zero-width nonbreaking space (ZWNBSP). 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The character is breakable white space. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The character is not breakable white space. 

</td>
</tr>
</table>
 


### -field fCharStop

Value indicating if the character is a valid position for showing the caret upon a character movement keyboard action. Possible values are defined in the following table. This member is set for most characters, but not on code points inside Indian and Southeast Asian character clusters. This member can be used to implement LEFT ARROW and RIGHT ARROW operations in editors.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The character is a valid position for showing the caret upon a character movement keyboard action. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The character is not a valid position for showing the caret upon a character movement keyboard action.

</td>
</tr>
</table>
 


### -field fWordStop

Value indicating the valid position for showing the caret upon a word movement keyboard action, such as CTRL+LEFT ARROW and CTRL+RIGHT ARROW. Possible values are defined in the following table. This member can be used to implement the CTRL+LEFT ARROW and CTRL+RIGHT ARROW operations in editors.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The character is a valid position for showing the caret upon a word movement keyboard action. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The character is not a valid position for showing the caret upon a word movement keyboard action.

</td>
</tr>
</table>
 


### -field fInvalid

Value used to mark characters that form an invalid or undisplayable combination. Possible values are defined in the following table. A script that can set this member has the <b>fInvalidLogAttr</b> member set in its <a href="https://msdn.microsoft.com/473c1265-1c2c-48f3-a852-c701bebcf9eb">SCRIPT_PROPERTIES</a> structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The character forms an invalid or undisplayable combination. 

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The character does not form an invalid or undisplayable combination.

</td>
</tr>
</table>
 


### -field fReserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/473c1265-1c2c-48f3-a852-c701bebcf9eb">SCRIPT_PROPERTIES</a>



<a href="https://msdn.microsoft.com/1613819f-9473-4d9f-8a65-a109c9ef3f43">ScriptBreak</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

