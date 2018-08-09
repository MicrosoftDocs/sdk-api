---
UID: NS:winddi._WCRUN
title: "_WCRUN"
author: windows-sdk-content
description: The WCRUN structure describes a run of Unicode characters.
old-location: display\wcrun.htm
old-project: display
ms.assetid: 01a90280-a7cc-4726-b0a2-68121bdb4686
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: "*PWCRUN, PWCRUN, PWCRUN structure pointer [Display Devices], WCRUN, WCRUN structure [Display Devices], _WCRUN, display.wcrun, grstrcts_0ef325fa-6d74-4c0e-87e2-126c05560c5d.xml, winddi/PWCRUN, winddi/WCRUN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
tech.root: 
req.typenames: WCRUN, *PWCRUN
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - WCRUN
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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
 

 

