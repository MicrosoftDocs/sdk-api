---
UID: NF:ddrawgdi.DdReleaseDC
title: DdReleaseDC function (ddrawgdi.h)
description: Wrapper for the NtGdiDdReleaseDC function and releases a device context (DC) previously obtained through DdGetDC or GdiEntry7. GdiEntry8 is defined as an alias for this function.
helpviewer_keywords: ["DdReleaseDC","DdReleaseDC function [Windows API]","GdiEntry8","_dxgkernel_ddreleasedc","ddrawgdi/DdReleaseDC","ddrawgdi/GdiEntry8","winprog._dxgkernel_ddreleasedc","winui._dxgkernel_ddreleasedc"]
old-location: winprog\_dxgkernel_ddreleasedc.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddreleasedc.htm
ms.date: 12/05/2018
ms.keywords: DdReleaseDC, DdReleaseDC function [Windows API], GdiEntry8, _dxgkernel_ddreleasedc, ddrawgdi/DdReleaseDC, ddrawgdi/GdiEntry8, winprog._dxgkernel_ddreleasedc, winui._dxgkernel_ddreleasedc
req.header: ddrawgdi.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdReleaseDC
 - ddrawgdi/DdReleaseDC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddrawgdi.h
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - DdReleaseDC
 - GdiEntry8
---

# DdReleaseDC function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddreleasedc">NtGdiDdReleaseDC</a> function and releases a device context (DC) previously obtained through <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddgetdc">DdGetDC</a> or <b>GdiEntry7</b>.


<b>GdiEntry8</b> is defined as an alias for this function.

## -parameters

### -param pSurfaceLocal

Pointer to the DirectDraw surface for which a DC was obtained.

## -returns

If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

Applications that need to obtain a DC for a DirectDraw surface can  use <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">IDirectDrawSurface7::GetDC</a>, which exposes this functionality in a manner independent of the operating system.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>