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

# TTVALIDATIONTESTSPARAMS structure


## -description



The <b>TTVALIDATIONTESTSPARAMS</b> structure contains parameters for testing a Microsoft OpenType font.




## -struct-fields




### -field ulStructSize

Size, in bytes, of this structure. The client should set this value to <b>sizeof</b>(TTVALIDATIONTESTSPARAMS).


### -field lTestFromSize

First character point size to test. This value is the smallest font size (lower bound) of the font sizes to test.


### -field lTestToSize

Last character point size to test. This value is an largest font size (upper bound) of the font sizes to test.


### -field ulCharSet

Flag specifying the character set of the font to validate. This flag can have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>CHARSET_UNICODE</td>
<td>Unicode character set, requiring 16-bit-character encoding.</td>
</tr>
<tr>
<td>CHARSET_SYMBOL</td>
<td>Symbol character set, requiring 16-bit-character encoding.</td>
</tr>
</table>
 


### -field usReserved1

Currently not used.


### -field usCharCodeCount

If zero, test over all glyphs.


### -field pusCharCodeSet

Pointer to array of Unicode characters.


## -see-also




<a href="https://msdn.microsoft.com/fe60938b-c728-49a9-89b4-495b2364091a">TTRunValidationTests</a>



<a href="https://msdn.microsoft.com/03bcfb1a-6ed8-4e78-b3c8-64d29dc74dbc">TTVALIDATIONTESTSPARAMSEX</a>
 

 

