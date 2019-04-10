---
UID: NS:t2embapi.__unnamed_struct_2
title: TTVALIDATIONTESTSPARAMS (t2embapi.h)
author: windows-sdk-content
description: The TTVALIDATIONTESTSPARAMS structure contains parameters for testing a Microsoft OpenType font.
old-location: gdi\ttvalidationtestparams.htm
tech.root: gdi
ms.assetid: 901fd8e5-1602-4e20-9269-d0c3fe661e45
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TTVALIDATIONTESTSPARAMS, TTVALIDATIONTESTSPARAMS structure [Windows GDI], _win32_TTVALIDATIONTESTPARAMS, gdi.ttvalidationtestparams, t2embapi/TTVALIDATIONTESTSPARAMS
ms.topic: struct
req.header: t2embapi.h
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
 - T2embapi.h
api_name:
 - TTVALIDATIONTESTSPARAMS
product: Windows
targetos: Windows
req.typenames: TTVALIDATIONTESTSPARAMS
req.redist: 
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
 

 

