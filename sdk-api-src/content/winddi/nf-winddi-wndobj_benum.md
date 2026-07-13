---
UID: NF:winddi.WNDOBJ_bEnum
title: WNDOBJ_bEnum function (winddi.h)
description: The WNDOBJ_bEnum function obtains a batch of rectangles from the visible region of a window.
helpviewer_keywords: ["WNDOBJ_bEnum","WNDOBJ_bEnum function [Display Devices]","display.wndobj_benum","gdifncs_73e625c4-af7b-4e0e-aace-b930ca192444.xml","winddi/WNDOBJ_bEnum"]
old-location: display\wndobj_benum.htm
tech.root: display
ms.assetid: ad883ab5-6374-499e-9144-e5b85feaa471
ms.date: 12/05/2018
ms.keywords: WNDOBJ_bEnum, WNDOBJ_bEnum function [Display Devices], display.wndobj_benum, gdifncs_73e625c4-af7b-4e0e-aace-b930ca192444.xml, winddi/WNDOBJ_bEnum
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WNDOBJ_bEnum
 - winddi/WNDOBJ_bEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - WNDOBJ_bEnum
---

# WNDOBJ_bEnum function


## -description

The <b>WNDOBJ_bEnum</b> function obtains a batch of rectangles from the visible region of a window.

## -parameters

### -param pwo

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a> structure created by a call to <a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a>.

### -param cj

Specifies the size, in bytes, of the buffer pointed to by <i>pul</i>. GDI will not write beyond this limit.

### -param pul

Pointer to the buffer in which a structure of the following form is to be written. In this structure, <b>c</b> is a count of the rectangles returned, and <b>arcl</b> is an array of rectangles:


```
typedef struct _ENUMRECTS{
    ULONG c;
    RECTL arcl[]
} ENUMRECTS;
```

## -returns

The return value is <b>TRUE</b> if there is more data to be enumerated and the driver should repeat the call. It is <b>FALSE</b> if the enumeration is complete.

## -remarks

The order of enumeration is determined by the call to <a href="/windows/desktop/api/winddi/nf-winddi-wndobj_cenumstart">WNDOBJ_cEnumStart</a>.

A possible loop structure for calling this function follows.


```
do {
    bMore = WNDOBJ_bEnum(pwo, sizeof(buffer), &buffer.c);
    for (i = 0; i < buffer.c; i++) { 
        //  Process the data
    }
} while (bMore);
```


<b>WNDOBJ_bEnum</b> should be called only by the callback function provided to GDI by the <a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a> function, or by the graphics DDI functions that are given a WNDOBJ.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-engcreatewnd">EngCreateWnd</a>



<a href="/windows/desktop/api/winddi/ns-winddi-wndobj">WNDOBJ</a>



<a href="/windows/desktop/api/winddi/nf-winddi-wndobj_cenumstart">WNDOBJ_cEnumStart</a>