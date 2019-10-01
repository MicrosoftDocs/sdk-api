---
UID: NS:winddi._WCRUN
title: WCRUN (winddi.h)
author: windows-sdk-content
description: The WCRUN structure describes a run of Unicode characters.
old-location: display\wcrun.htm
tech.root: display
ms.assetid: 01a90280-a7cc-4726-b0a2-68121bdb4686
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PWCRUN, PWCRUN, PWCRUN structure pointer [Display Devices], WCRUN, WCRUN structure [Display Devices], display.wcrun, grstrcts_0ef325fa-6d74-4c0e-87e2-126c05560c5d.xml, winddi/PWCRUN, winddi/WCRUN'
ms.topic: struct
f1_keywords:
- winddi/WCRUN
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- winddi.h
api_name:
- WCRUN
targetos: Windows
req.typenames: WCRUN, *PWCRUN
req.redist: 
ms.custom: 19H1
---

# WCRUN structure


## -description


The WCRUN structure describes a run of Unicode characters.


## -struct-fields




### -field wcLow

Specifies the first character in the run.


### -field cGlyphs

Specifies the count of characters in the run.


### -field phg

Pointer to an array of glyph handles that correspond to this run. If this member is <b>NULL</b>, then each character in this run can be converted to a glyph handle by a cast, as in the following example:


```
HGLYPH hg = (HGLYPH) wc;
```



## -remarks



GDI relies on the runs being arranged in increasing order by code points. A binary search is made through the list of runs.

The <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a> structure contains a WCRUN structure as one of its members.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-drvqueryfonttree">DrvQueryFontTree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-fd_glyphset">FD_GLYPHSET</a>
 

 

