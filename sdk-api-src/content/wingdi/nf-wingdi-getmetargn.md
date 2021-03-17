---
UID: NF:wingdi.GetMetaRgn
title: GetMetaRgn function (wingdi.h)
description: The GetMetaRgn function retrieves the current metaregion for the specified device context.
helpviewer_keywords: ["GetMetaRgn","GetMetaRgn function [Windows GDI]","_win32_GetMetaRgn","gdi.getmetargn","wingdi/GetMetaRgn"]
old-location: gdi\getmetargn.htm
tech.root: gdi
ms.assetid: 9c2741cf-30e4-4100-bae9-ad99a7ae37f1
ms.date: 12/05/2018
ms.keywords: GetMetaRgn, GetMetaRgn function [Windows GDI], _win32_GetMetaRgn, gdi.getmetargn, wingdi/GetMetaRgn
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
 - GetMetaRgn
 - wingdi/GetMetaRgn
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
 - GetMetaRgn
---

# GetMetaRgn function


## -description

The <b>GetMetaRgn</b> function retrieves the current metaregion for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hrgn [in]

A handle to an existing region before the function is called. After the function returns, this parameter is a handle to a copy of the current metaregion.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.

## -remarks

If the function succeeds, <i>hrgn</i> is a handle to a copy of the current metaregion. Subsequent changes to this copy will not affect the current metaregion.

The current clipping region of a device context is defined by the intersection of its clipping region and its metaregion.

## -see-also

<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-setmetargn">SetMetaRgn</a>