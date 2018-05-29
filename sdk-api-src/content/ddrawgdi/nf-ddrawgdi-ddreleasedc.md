---
UID: NF:ddrawgdi.DdReleaseDC
title: DdReleaseDC function
author: windows-sdk-content
description: Wrapper for the NtGdiDdReleaseDC function and releases a device context (DC) previously obtained through DdGetDC or GdiEntry7. GdiEntry8 is defined as an alias for this function.
old-location: winprog\_dxgkernel_ddreleasedc.htm
old-project: DevNotes
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddreleasedc.htm
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: DdReleaseDC, DdReleaseDC function [Windows API], GdiEntry8, _dxgkernel_ddreleasedc, ddrawgdi/DdReleaseDC, ddrawgdi/GdiEntry8, winprog._dxgkernel_ddreleasedc, winui._dxgkernel_ddreleasedc
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
req.typenames: "*LPDDSURFACEDESC2, DDSURFACEDESC2"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ddrawgdi.h
-	Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
-	GDI32.dll
-	GDI32Full.dll
api_name:
-	DdReleaseDC
-	GdiEntry8
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DdReleaseDC function


## -description


<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="https://msdn.microsoft.com/98def2a1-878d-4776-a519-32cb70107338">NtGdiDdReleaseDC</a> function and releases a device context (DC) previously obtained through <a href="https://msdn.microsoft.com/0f8872d2-adfa-4bbc-af27-884def677f0b">DdGetDC</a> or <b>GdiEntry7</b>.


<b>GdiEntry8</b> is defined as an alias for this function.


## -parameters




### -param pSurfaceLocal

Pointer to the DirectDraw surface for which a DC was obtained.


## -returns



If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.




## -remarks



Applications that need to obtain a DC for a DirectDraw surface can  use <a href="https://msdn.microsoft.com/683be1bc-8232-42de-907f-1136ffdd524d">IDirectDrawSurface7::GetDC</a>, which exposes this functionality in a manner independent of the operating system.
        




## -see-also




<a href="https://msdn.microsoft.com/96d11d10-dd21-4e2b-a30d-fe29d24eeba6">Graphics Low Level Client Support</a>
 

 

