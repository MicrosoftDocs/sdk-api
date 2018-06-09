---
UID: NF:ddrawgdi.DdGetDC
title: DdGetDC function
author: windows-sdk-content
description: Wrapper for the NtGdiDdGetDC function and returns a Windows Graphics Device Interface (GDI)  device context (DC) that represents the Microsoft DirectDraw surface indicated. GdiEntry7 is defined as an alias for this function.
old-location: winprog\_dxgkernel_ddgetdc.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddgetdc.htm
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DdGetDC, DdGetDC function [Windows API], GdiEntry7, _dxgkernel_ddgetdc, ddrawgdi/DdGetDC, ddrawgdi/GdiEntry7, winprog._dxgkernel_ddgetdc, winui._dxgkernel_ddgetdc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: "*LPDDSURFACEDESC2, DDSURFACEDESC2"
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DdGetDC function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4">NtGdiDdGetDC</a> function and returns a Windows Graphics Device Interface (GDI) 
   device context (DC) that represents the Microsoft DirectDraw surface indicated.


<b>GdiEntry7</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the DirectDraw surface for which a DC is requested.


### -param pColorTable

Optional pointer to a 256-entry array of <a href="https://msdn.microsoft.com/6430e7cf-c9f2-4376-8b17-28c10d9d0f00">PALETTEENTRY</a> structures. If the color table is null, and the surface and display mode are both 8 bits per pixel, the DC shares the color table of the device.


## -returns



If successful, this function returns a valid <b>HDC</b>; otherwise it returns <b>NULL</b>.




## -remarks



If both the surface and the current display mode are palletized at 8 bits per pixel, the DC can be given the special property that its color table is shared by the color table of the display device. Applications are advised to call <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a> instead, which provides the same functionality in a manner independent of the operating system.


The returned DC must be freed by a call to <a href="https://msdn.microsoft.com/98def2a1-878d-4776-a519-32cb70107338">NtGdiDdReleaseDC</a> or <b>GdiEntry8</b>.





## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

