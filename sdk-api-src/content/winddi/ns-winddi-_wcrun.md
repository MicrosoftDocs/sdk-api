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

# _WCRUN structure


## -description


The WCRUN structure describes a run of Unicode characters.


## -struct-fields




### -field wcLow

Specifies the first character in the run.


### -field cGlyphs

Specifies the count of characters in the run.


### -field phg

Pointer to an array of glyph handles that correspond to this run. If this member is <b>NULL</b>, then each character in this run can be converted to a glyph handle by a cast, as in the following example:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>HGLYPH hg = (HGLYPH) wc;</pre>
</td>
</tr>
</table></span></div>

## -remarks



GDI relies on the runs being arranged in increasing order by code points. A binary search is made through the list of runs.

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff565625">FD_GLYPHSET</a> structure contains a WCRUN structure as one of its members.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556266">DrvQueryFontTree</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565625">FD_GLYPHSET</a>
 

 

