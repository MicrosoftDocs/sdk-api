---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# tag_SCRIPT_DIGITSUBSTITUTE structure


## -description



Contains native digit and digit substitution settings.




## -struct-fields




### -field NationalDigitLanguage

Language for native substitution.


### -field TraditionalDigitLanguage

Language for traditional substitution.


### -field DigitSubstitute

Substitution type. This member is normally set by <a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>. However, it can also have any of the values defined in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_CONTEXT_"></a><a id="script_digitsubstitute_context_"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_CONTEXT </b></dt>
</dl>
</td>
<td width="60%">
Substitute digits U+0030 to U+0039 using the language of the prior letters. If there are no prior letters, substitute digits using the <b>TraditionalDigitLanguage</b> member. This member is normally set to the primary language of the locale passed to <a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_NATIONAL"></a><a id="script_digitsubstitute_national"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_NATIONAL</b></dt>
</dl>
</td>
<td width="60%">
Substitute digits U+0030 to U+0039 using the <b>NationalDigitLanguage</b> member. This member is normally set to the national digits retrieved for the constant <a href="https://msdn.microsoft.com/560978d7-a33c-4e62-9abd-cbd3ec38f3b5">LOCALE_SNATIVEDIGITS</a> by <a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_NONE"></a><a id="script_digitsubstitute_none"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_NONE</b></dt>
</dl>
</td>
<td width="60%">
Do not substitute digits. Display Unicode values U+0030 to U+0039 with European numerals.

</td>
</tr>
<tr>
<td width="40%"><a id="SCRIPT_DIGITSUBSTITUTE_TRADITIONAL"></a><a id="script_digitsubstitute_traditional"></a><dl>
<dt><b>SCRIPT_DIGITSUBSTITUTE_TRADITIONAL</b></dt>
</dl>
</td>
<td width="60%">
Substitute digits U+0030 to U+0039 using the <b>TraditionalDigitLanguage</b> member. This member is normally set to the primary language of the locale passed to <a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>.

</td>
</tr>
</table>
 


### -field dwReserved

Reserved; initialize to 0.


## -see-also




<a href="https://msdn.microsoft.com/6b5267d8-b102-410c-bdc9-831555ca2f84">Digit Shapes</a>



<a href="https://msdn.microsoft.com/2c8c33d5-5cd6-4734-bf44-af7d4b578672">ScriptRecordDigitSubstitution</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

