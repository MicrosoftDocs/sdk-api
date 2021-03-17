---
UID: NF:ddrawgdi.DdGetDC
title: DdGetDC function (ddrawgdi.h)
description: Wrapper for the NtGdiDdGetDC function and returns a Windows Graphics Device Interface (GDI)  device context (DC) that represents the Microsoft DirectDraw surface indicated. GdiEntry7 is defined as an alias for this function.
helpviewer_keywords: ["DdGetDC","DdGetDC function [Windows API]","GdiEntry7","_dxgkernel_ddgetdc","ddrawgdi/DdGetDC","ddrawgdi/GdiEntry7","winprog._dxgkernel_ddgetdc","winui._dxgkernel_ddgetdc"]
old-location: winprog\_dxgkernel_ddgetdc.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddgetdc.htm
ms.date: 12/05/2018
ms.keywords: DdGetDC, DdGetDC function [Windows API], GdiEntry7, _dxgkernel_ddgetdc, ddrawgdi/DdGetDC, ddrawgdi/GdiEntry7, winprog._dxgkernel_ddgetdc, winui._dxgkernel_ddgetdc
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
 - DdGetDC
 - ddrawgdi/DdGetDC
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
 - DdGetDC
 - GdiEntry7
---

# DdGetDC function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddgetdc">NtGdiDdGetDC</a> function and returns a Windows Graphics Device Interface (GDI) 
   device context (DC) that represents the Microsoft DirectDraw surface indicated.


<b>GdiEntry7</b> is defined as an alias for this function.

## -parameters

### -param pSurfaceLocal

Pointer to the DirectDraw surface for which a DC is requested.

### -param pColorTable

Optional pointer to a 256-entry array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures. If the color table is null, and the surface and display mode are both 8 bits per pixel, the DC shares the color table of the device.

## -returns

If successful, this function returns a valid <b>HDC</b>; otherwise it returns <b>NULL</b>.

## -remarks

If both the surface and the current display mode are palletized at 8 bits per pixel, the DC can be given the special property that its color table is shared by the color table of the display device. Applications are advised to call <a href="/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc">IDirectDrawSurface7::GetDC</a> instead, which provides the same functionality in a manner independent of the operating system.


The returned DC must be freed by a call to <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddreleasedc">NtGdiDdReleaseDC</a> or <b>GdiEntry8</b>.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>