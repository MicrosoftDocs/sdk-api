---
UID: NF:dcomp.IDCompositionDesktopDevice.CreateSurfaceFromHwnd
title: IDCompositionDesktopDevice::CreateSurfaceFromHwnd
author: windows-sdk-content
description: Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.
old-location: directcomp\idcompositiondesktopdevice_createsurfacefromhwnd.htm
tech.root: directcomp
ms.assetid: 89A4F321-26BE-4175-A052-FE5734DDB524
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateSurfaceFromHwnd, CreateSurfaceFromHwnd method [DirectComposition], CreateSurfaceFromHwnd method [DirectComposition],IDCompositionDesktopDevice interface, IDCompositionDesktopDevice interface [DirectComposition],CreateSurfaceFromHwnd method, IDCompositionDesktopDevice.CreateSurfaceFromHwnd, IDCompositionDesktopDevice::CreateSurfaceFromHwnd, dcomp/IDCompositionDesktopDevice::CreateSurfaceFromHwnd, directcomp.idcompositiondesktopdevice_createsurfacefromhwnd
ms.prod: windows-hardware
ms.technology: windows-devices
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




### -param hwnd

TBD


### -param surface [out]

The new composition surface object. This parameter must not be NULL.



#### - handle [in]

The handle of the layered window for which to create a wrapper. A layered window is created by specifying WS_EX_LAYERED when creating the window with the <a href="https://msdn.microsoft.com/33deeb92-6285-4c67-9338-ca2e194b9915">CreateWindowEx</a> function or by setting WS_EX_LAYERED via <a href="https://msdn.microsoft.com/75f6721f-188c-4daa-9410-6cb2d86869fc">SetWindowLong</a> after the window has been created.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



You can use the surface pointer in calls to the IDCompositionVisual::SetContent method to set the content of one or more visuals. After setting the content, the visuals compose the contents of the specified layered window as long as the window is layered. If the window is unlayered, the window content disappears from the output of the composition tree. If the window is later re-layered, the window content reappears as long as it is still associated with a visual. If the window is resized, the affected visuals are re-composed.



The contents of the window are not cached beyond the life of the window. That is, if the window is destroyed, the affected visuals stop composing the window.



If the window is moved off-screen or resized to zero, the system stops composing the content of those visuals. You should use the <a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a> function with the DWMWA_CLOAK flag to "cloak" the layered child window when you need to hide the original window while allowing the system to continue to compose the content of the visuals.





## -see-also




<a href="https://msdn.microsoft.com/0FCDCDC2-541A-4EB5-A7FF-492AB5C25F7B">IDCompositionDesktopDevice</a>



<a href="https://msdn.microsoft.com/894E6E30-6C28-476D-9AE5-D0664A69E03C">IDCompositionVisual::SetContent</a>
 

 

