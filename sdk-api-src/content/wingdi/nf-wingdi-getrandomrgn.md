---
UID: NF:wingdi.GetRandomRgn
title: GetRandomRgn function (wingdi.h)
description: The GetRandomRgn function copies the system clipping region of a specified device context to a specific region.
helpviewer_keywords: ["GetRandomRgn","GetRandomRgn function [Windows GDI]","_win32_GetRandomRgn","gdi.getrandomrgn","wingdi/GetRandomRgn"]
old-location: gdi\getrandomrgn.htm
tech.root: gdi
ms.assetid: a7527d7a-7b5e-4dd5-9270-94bc92b5a4a0
ms.date: 12/05/2018
ms.keywords: GetRandomRgn, GetRandomRgn function [Windows GDI], _win32_GetRandomRgn, gdi.getrandomrgn, wingdi/GetRandomRgn
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
 - GetRandomRgn
 - wingdi/GetRandomRgn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-Rgn-L1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - GetRandomRgn
---

# GetRandomRgn function


## -description

The <b>GetRandomRgn</b> function copies the system clipping region of a specified device context to a specific region.

## -parameters

### -param hdc [in]

A handle to the device context.

### -param hrgn [in]

A handle to a region. Before the function is called, this identifies an existing region. After the function returns, this identifies a copy of the current system region. The old region identified by <i>hrgn</i> is overwritten.

### -param i [in]

This parameter must be SYSRGN.

## -returns

If the function succeeds, the return value is 1. If the function fails, the return value is -1. If the region to be retrieved is <b>NULL</b>, the return value is 0. If the function fails or the region to be retrieved is <b>NULL</b>, <i>hrgn</i> is not initialized.

## -remarks

When using the SYSRGN flag, note that the system clipping region might not be current because of window movements. Nonetheless, it is safe to retrieve and use the system clipping region within the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>-<a href="/windows/desktop/api/winuser/nf-winuser-endpaint">EndPaint</a> block during <a href="/windows/desktop/gdi/wm-paint">WM_PAINT</a> processing. In this case, the system region is the intersection of the update region and the current visible area of the window. Any window movement following the return of <b>GetRandomRgn</b> and before <b>EndPaint</b> will result in a new <b>WM_PAINT</b> message. Any other use of the SYSRGN flag may result in painting errors in your application.

The region returned is in screen coordinates.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="/windows/desktop/gdi/clipping-functions">Clipping Functions</a>



<a href="/windows/desktop/gdi/clipping">Clipping Overview</a>



<a href="/windows/desktop/api/winuser/nf-winuser-endpaint">EndPaint</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-extselectcliprgn">ExtSelectClipRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getclipbox">GetClipBox</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getcliprgn">GetClipRgn</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-offsetrgn">OffsetRgn</a>