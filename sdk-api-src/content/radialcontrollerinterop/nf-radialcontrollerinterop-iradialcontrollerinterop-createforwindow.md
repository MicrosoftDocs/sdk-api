---
UID: NF:radialcontrollerinterop.IRadialControllerInterop.CreateForWindow
title: IRadialControllerInterop::CreateForWindow (radialcontrollerinterop.h)
description: Instantiates a RadialController object and binds it to the active application.
helpviewer_keywords: ["CreateForWindow","CreateForWindow method","CreateForWindow method","IRadialControllerInterop interface","IRadialControllerInterop interface","CreateForWindow method","IRadialControllerInterop.CreateForWindow","IRadialControllerInterop::CreateForWindow","Input_Radial.iradialcontrollerinterop_createforwindow","radialcontrollerinterop/IRadialControllerInterop::CreateForWindow"]
old-location: input_radial\iradialcontrollerinterop_createforwindow.htm
tech.root: winrt
ms.assetid: fe419ce2-9767-42c4-aaa6-a9b9ea93ec3e
ms.date: 12/05/2018
ms.keywords: CreateForWindow, CreateForWindow method, CreateForWindow method,IRadialControllerInterop interface, IRadialControllerInterop interface,CreateForWindow method, IRadialControllerInterop.CreateForWindow, IRadialControllerInterop::CreateForWindow, Input_Radial.iradialcontrollerinterop_createforwindow, radialcontrollerinterop/IRadialControllerInterop::CreateForWindow
req.header: radialcontrollerinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RadialControllerInterop.idl
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
 - IRadialControllerInterop::CreateForWindow
 - radialcontrollerinterop/IRadialControllerInterop::CreateForWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RadialControllerInterop.h
api_name:
 - IRadialControllerInterop.CreateForWindow
---

# IRadialControllerInterop::CreateForWindow


## -description

Instantiates a <a href="/uwp/api/windows.ui.input.radialcontroller">RadialController</a> object and binds it to the active application.

## -parameters

### -param hwnd [in]

Handle to the window of the active application.

### -param riid [in]

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example, __uuidof(IRadialController) will get the GUID of the interface to a buffer resource.

### -param ppv [out]

Address of a pointer to a <a href="/uwp/api/windows.ui.input.radialcontroller">RadialController</a> object.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Developer and UX guidance</b>



<a href="/previous-versions/windows/desktop/api/radialcontrollerinterop/nn-radialcontrollerinterop-iradialcontrollerinterop">IRadialControllerInterop</a>



<b>Samples</b>



<a href="/windows/uwp/design/input/windows-wheel-interactions">Surface Dial interactions</a>



<a href="https://github.com/Microsoft/Windows-universal-samples/tree/b78d95134ce2d57c848e0a8dc339fc362748fb9c/Samples/RadialController">Universal Windows Platform samples (C# and C++)</a>



<a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/RadialController">Windows classic desktop sample</a>