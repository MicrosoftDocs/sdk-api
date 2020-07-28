---
UID: NF:winddi.CLIPOBJ_bEnum
title: CLIPOBJ_bEnum function (winddi.h)
description: The CLIPOBJ_bEnum function enumerates a batch of rectangles from a specified clip region; a prior call to CLIPOBJ_cEnumStart determines the order of enumeration.
helpviewer_keywords: ["CLIPOBJ_bEnum","CLIPOBJ_bEnum function [Display Devices]","display.clipobj_benum","gdifncs_8f383214-6bb4-4099-bdf7-c019a28ef8ac.xml","winddi/CLIPOBJ_bEnum"]
old-location: display\clipobj_benum.htm
tech.root: display
ms.assetid: d54e6e2a-4869-45d6-9ad1-4e9aca5f5e77
ms.date: 12/05/2018
ms.keywords: CLIPOBJ_bEnum, CLIPOBJ_bEnum function [Display Devices], display.clipobj_benum, gdifncs_8f383214-6bb4-4099-bdf7-c019a28ef8ac.xml, winddi/CLIPOBJ_bEnum
f1_keywords:
- winddi/CLIPOBJ_bEnum
dev_langs:
- c++
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Win32k.sys
api_name:
- CLIPOBJ_bEnum
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CLIPOBJ_bEnum function


## -description


The <b>CLIPOBJ_bEnum</b> function enumerates a batch of rectangles from a specified <a href="https://docs.microsoft.com/windows-hardware/drivers/">clip region</a>; a prior call to <a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-clipobj_cenumstart">CLIPOBJ_cEnumStart</a> determines the order of enumeration.


## -parameters




### -param pco [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a> structure describing the clip region that is to be enumerated.


### -param cj [in]

Specifies the size, in bytes, of the buffer pointed to by <i>pv</i>.


### -param pul [out]

Pointer to the buffer that will receive data about the clip region in an <a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-enumrects">ENUMRECTS</a> structure.


## -returns



The return value is <b>TRUE</b> if the driver must call this function again for more enumeration data, or <b>FALSE</b> if the enumeration is complete. It is possible for <b>CLIPOBJ_bEnum</b> to return <b>TRUE</b> with the number of clipping rectangles equal to zero. In such cases, the driver should call <b>CLIPOBJ_bEnum</b> again without taking any action.




## -remarks



A possible loop structure for calling this function follows:


```
do {
    bMore = CLIPOBJ_bEnum(pco, sizeof(buffer), &buffer.c);
    for (i = 0; i < buffer.c; i++) {
        .
        .
        .
    }
} while (bMore);
```


The count of objects written to the buffer is written to the buffer itself.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-clipobj">CLIPOBJ</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/nf-winddi-clipobj_cenumstart">CLIPOBJ_cEnumStart</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winddi/ns-winddi-enumrects">ENUMRECTS</a>
 

 

