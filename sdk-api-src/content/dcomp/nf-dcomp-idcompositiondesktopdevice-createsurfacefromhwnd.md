---
UID: NF:dcomp.IDCompositionDesktopDevice.CreateSurfaceFromHwnd
title: IDCompositionDesktopDevice::CreateSurfaceFromHwnd
author: windows-sdk-content
description: Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.
old-location: directcomp\idcompositiondesktopdevice_createsurfacefromhwnd.htm
tech.root: directcomp
ms.assetid: 89A4F321-26BE-4175-A052-FE5734DDB524
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateSurfaceFromHwnd, CreateSurfaceFromHwnd method [DirectComposition], CreateSurfaceFromHwnd method [DirectComposition],IDCompositionDesktopDevice interface, IDCompositionDesktopDevice interface [DirectComposition],CreateSurfaceFromHwnd method, IDCompositionDesktopDevice.CreateSurfaceFromHwnd, IDCompositionDesktopDevice::CreateSurfaceFromHwnd, dcomp/IDCompositionDesktopDevice::CreateSurfaceFromHwnd, directcomp.idcompositiondesktopdevice_createsurfacefromhwnd
ms.topic: method
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dcomp.h
api_name:
 - IDCompositionDesktopDevice.CreateSurfaceFromHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDesktopDevice::CreateSurfaceFromHwnd


## -description


Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.


## -parameters




### -param hwnd [in]

The handle of the layered window for which to create a wrapper. A layered window is created by specifying WS_EX_LAYERED when creating the window with the <a href="https://msdn.microsoft.com/en-us/library/ms632680(v=VS.85).aspx">CreateWindowEx</a> function or by setting WS_EX_LAYERED via <a href="https://msdn.microsoft.com/en-us/library/ms633591(v=VS.85).aspx">SetWindowLong</a> after the window has been created.


### -param surface [out]

The new composition surface object. This parameter must not be NULL.



## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



You can use the surface pointer in calls to the IDCompositionVisual::SetContent method to set the content of one or more visuals. After setting the content, the visuals compose the contents of the specified layered window as long as the window is layered. If the window is unlayered, the window content disappears from the output of the composition tree. If the window is later re-layered, the window content reappears as long as it is still associated with a visual. If the window is resized, the affected visuals are re-composed.



The contents of the window are not cached beyond the life of the window. That is, if the window is destroyed, the affected visuals stop composing the window.



If the window is moved off-screen or resized to zero, the system stops composing the content of those visuals. You should use the <a href="https://msdn.microsoft.com/en-us/library/Aa969524(v=VS.85).aspx">DwmSetWindowAttribute</a> function with the DWMWA_CLOAK flag to "cloak" the layered child window when you need to hide the original window while allowing the system to continue to compose the content of the visuals.





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280350(v=VS.85).aspx">IDCompositionDesktopDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449157(v=VS.85).aspx">IDCompositionVisual::SetContent</a>
 

 

