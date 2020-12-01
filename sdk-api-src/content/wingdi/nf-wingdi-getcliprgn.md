---
UID: NF:wingdi.GetClipRgn
title: GetClipRgn function (wingdi.h)
description: The GetClipRgn function retrieves a handle identifying the current application-defined clipping region for the specified device context.
helpviewer_keywords: ["GetClipRgn","GetClipRgn function [Windows GDI]","_win32_GetClipRgn","gdi.getcliprgn","wingdi/GetClipRgn"]
old-location: gdi\getcliprgn.htm
tech.root: gdi
ms.assetid: 66c807b8-129f-40f2-b8d8-995e0a5e22e4
ms.date: 12/05/2018
ms.keywords: GetClipRgn, GetClipRgn function [Windows GDI], _win32_GetClipRgn, gdi.getcliprgn, wingdi/GetClipRgn
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
 - GetClipRgn
 - wingdi/GetClipRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - ext-ms-win-gdi-clipping-l1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetClipRgn
---

# GetClipRgn function


## -description

The <b>GetClipRgn</b> function retrieves a handle identifying the current application-defined clipping region for the specified device context.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hrgn [in]

A handle to an existing region before the function is called. After the function returns, this parameter is a handle to a copy of the current clipping region.

## -returns

If the function succeeds and there is no clipping region for the given device context, the return value is zero. If the function succeeds and there is a clipping region for the given device context, the return value is 1. If an error occurs, the return value is -1.

## -remarks

An application-defined clipping region is a clipping region identified by the <a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a> function. It is not a clipping region created when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function.

If the function succeeds, the <i>hrgn</i> parameter is a handle to a copy of the current clipping region. Subsequent changes to this copy will not affect the current clipping region.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-selectcliprgn">SelectClipRgn</a>