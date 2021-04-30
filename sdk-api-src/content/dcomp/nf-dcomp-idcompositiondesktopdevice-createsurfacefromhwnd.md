---
UID: NF:dcomp.IDCompositionDesktopDevice.CreateSurfaceFromHwnd
title: IDCompositionDesktopDevice::CreateSurfaceFromHwnd (dcomp.h)
description: Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.
helpviewer_keywords: ["CreateSurfaceFromHwnd","CreateSurfaceFromHwnd method [DirectComposition]","CreateSurfaceFromHwnd method [DirectComposition]","IDCompositionDesktopDevice interface","IDCompositionDesktopDevice interface [DirectComposition]","CreateSurfaceFromHwnd method","IDCompositionDesktopDevice.CreateSurfaceFromHwnd","IDCompositionDesktopDevice::CreateSurfaceFromHwnd","dcomp/IDCompositionDesktopDevice::CreateSurfaceFromHwnd","directcomp.idcompositiondesktopdevice_createsurfacefromhwnd"]
old-location: directcomp\idcompositiondesktopdevice_createsurfacefromhwnd.htm
tech.root: directcomp
ms.assetid: 89A4F321-26BE-4175-A052-FE5734DDB524
ms.date: 12/05/2018
ms.keywords: CreateSurfaceFromHwnd, CreateSurfaceFromHwnd method [DirectComposition], CreateSurfaceFromHwnd method [DirectComposition],IDCompositionDesktopDevice interface, IDCompositionDesktopDevice interface [DirectComposition],CreateSurfaceFromHwnd method, IDCompositionDesktopDevice.CreateSurfaceFromHwnd, IDCompositionDesktopDevice::CreateSurfaceFromHwnd, dcomp/IDCompositionDesktopDevice::CreateSurfaceFromHwnd, directcomp.idcompositiondesktopdevice_createsurfacefromhwnd
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDesktopDevice::CreateSurfaceFromHwnd
 - dcomp/IDCompositionDesktopDevice::CreateSurfaceFromHwnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dcomp.h
api_name:
 - IDCompositionDesktopDevice.CreateSurfaceFromHwnd
---

# IDCompositionDesktopDevice::CreateSurfaceFromHwnd


## -description

Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.

## -parameters

### -param hwnd [in]

The handle of the layered window for which to create a wrapper. A layered window is created by specifying WS_EX_LAYERED when creating the window with the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> function or by setting WS_EX_LAYERED via <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga">SetWindowLong</a> after the window has been created.

### -param surface [out]

The new composition surface object. This parameter must not be NULL.

## -returns

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

You can use the surface pointer in calls to the IDCompositionVisual::SetContent method to set the content of one or more visuals. After setting the content, the visuals compose the contents of the specified layered window as long as the window is layered. If the window is unlayered, the window content disappears from the output of the composition tree. If the window is later re-layered, the window content reappears as long as it is still associated with a visual. If the window is resized, the affected visuals are re-composed.



The contents of the window are not cached beyond the life of the window. That is, if the window is destroyed, the affected visuals stop composing the window.



If the window is moved off-screen or resized to zero, the system stops composing the content of those visuals. You should use the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute">DwmSetWindowAttribute</a> function with the DWMWA_CLOAK flag to "cloak" the layered child window when you need to hide the original window while allowing the system to continue to compose the content of the visuals.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondesktopdevice">IDCompositionDesktopDevice</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-setcontent">IDCompositionVisual::SetContent</a>