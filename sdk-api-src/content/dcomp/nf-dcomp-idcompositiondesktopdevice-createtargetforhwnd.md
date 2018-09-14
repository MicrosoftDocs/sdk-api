---
UID: NF:dcomp.IDCompositionDesktopDevice.CreateTargetForHwnd
title: IDCompositionDesktopDevice::CreateTargetForHwnd
author: windows-sdk-content
description: Creates a composition target object that is bound to the window that is represented by the specified window handle.
old-location: directcomp\idcompositiondesktopdevice_createtargetforhwnd.htm
tech.root: directcomp
ms.assetid: F3296B55-9A0B-4A31-90E4-05E2DF7B9B15
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CreateTargetForHwnd, CreateTargetForHwnd method [DirectComposition], CreateTargetForHwnd method [DirectComposition],IDCompositionDesktopDevice interface, IDCompositionDesktopDevice interface [DirectComposition],CreateTargetForHwnd method, IDCompositionDesktopDevice.CreateTargetForHwnd, IDCompositionDesktopDevice::CreateTargetForHwnd, dcomp/IDCompositionDesktopDevice::CreateTargetForHwnd, directcomp.idcompositiondesktopdevice_createtargetforhwnd
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
 - IDCompositionDesktopDevice.CreateTargetForHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDesktopDevice::CreateTargetForHwnd


## -description


Creates a composition target object that is bound to the window that is represented by the specified window handle.


## -parameters




### -param hwnd [in]

The window to which the composition target object should be bound. This parameter must not be NULL.


### -param topmost

TRUE if the visual tree should be displayed on top of the children of the window specified by the hwnd parameter; otherwise, the visual tree is displayed behind the children.


### -param target [out]

The new composition target object. This parameter must not be NULL.


## -returns



If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A DirectComposition visual tree must be bound to a window before anything can be displayed on screen. The window can be a top-level window or a child window. In either case, the window can be a layered window, but in all cases the window must belong to the calling process. If the window belongs to a different process, this method returns <a href="directcomposition_error_codes.htm">DCOMPOSITION_ERROR_ACCESS_DENIED</a>.

When DirectComposition content is composed to the window, the content is always composed on top of whatever is drawn directly to that window through the device context returned by the <a href="https://msdn.microsoft.com/50b2387b-c8e4-42a8-8f0f-0bdb355adbfd">GetDC</a> function, or by calls to DirectX Present methods. However, because window clipping rules apply to DirectComposition content, if the window has child windows, those child windows may clip the visual tree. The topmost parameter determines whether child windows clip the visual tree.

Conceptually, each window consists of four layers:

<ol>
<li>The contents drawn directly to the window handle (this is the bottommost layer).</li>
<li>An optional DirectComposition visual tree.</li>
<li>The contents of all child windows, if any.</li>
<li>Another optional DirectComposition visual tree (this is the topmost layer).</li>
</ol>
All four layers are clipped to the window’s visible region.

At most, only two composition targets can be created for each window in the system, one topmost and one not topmost. If a composition target is already bound to the specified window at the specified layer, this method fails. When a composition target object is destroyed, the layer it composed is available for use by a new composition target object.




## -see-also




<a href="https://msdn.microsoft.com/0FCDCDC2-541A-4EB5-A7FF-492AB5C25F7B">IDCompositionDesktopDevice</a>



<a href="https://msdn.microsoft.com/D4D04A43-BF00-482A-9CDD-A476BD1CB953">IDCompositionVisual2</a>
 

 

