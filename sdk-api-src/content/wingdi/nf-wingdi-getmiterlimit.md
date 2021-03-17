---
UID: NF:wingdi.GetMiterLimit
title: GetMiterLimit function (wingdi.h)
description: The GetMiterLimit function retrieves the miter limit for the specified device context.
helpviewer_keywords: ["GetMiterLimit","GetMiterLimit function [Windows GDI]","_win32_GetMiterLimit","gdi.getmiterlimit","wingdi/GetMiterLimit"]
old-location: gdi\getmiterlimit.htm
tech.root: gdi
ms.assetid: 51b1fb95-dd44-47f8-9311-2c6dc9c57bbc
ms.date: 12/05/2018
ms.keywords: GetMiterLimit, GetMiterLimit function [Windows GDI], _win32_GetMiterLimit, gdi.getmiterlimit, wingdi/GetMiterLimit
req.header: wingdi.h
req.include-header: Windows.h
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetMiterLimit
 - wingdi/GetMiterLimit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetMiterLimit
---

# GetMiterLimit function


## -description

The <b>GetMiterLimit</b> function retrieves the miter limit for the specified device context.

## -parameters

### -param hdc [in]

Handle to the device context.

### -param plimit [out]

Pointer to a floating-point value that receives the current miter limit.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

The miter limit is used when drawing geometric lines that have miter joins.

## -see-also

<a href="/windows/desktop/api/wingdi/nf-wingdi-extcreatepen">ExtCreatePen</a>



<a href="/windows/desktop/gdi/path-functions">Path Functions</a>



<a href="/windows/desktop/gdi/paths">Paths Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmiterlimit">SetMiterLimit</a>