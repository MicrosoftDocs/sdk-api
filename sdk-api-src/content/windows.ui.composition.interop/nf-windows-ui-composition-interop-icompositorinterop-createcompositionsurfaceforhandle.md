---
UID: NF:windows.ui.composition.interop.ICompositorInterop.CreateCompositionSurfaceForHandle
title: ICompositorInterop::CreateCompositionSurfaceForHandle (windows.ui.composition.interop.h)
description: Creates an instance of CompositionSurface for use with the handle of a swapchain. In order to host media swapchain on a CompositionSurface, use the IMFMediaEngineEx::GetVideoSwapchainHandle method.
helpviewer_keywords: ["CreateCompositionSurfaceForHandle","CreateCompositionSurfaceForHandle method","CreateCompositionSurfaceForHandle method","ICompositorInterop interface","ICompositorInterop interface","CreateCompositionSurfaceForHandle method","ICompositorInterop.CreateCompositionSurfaceForHandle","ICompositorInterop.composition","ICompositorInterop::CreateCompositionSurfaceForHandle","ICompositorInterop::composition","w_ui_comp.icompositorinterop_createcompositionsurfaceforhandle","windows/ICompositorInterop::CreateCompositionSurfaceForHandle"]
old-location: w_ui_comp\icompositorinterop_createcompositionsurfaceforhandle.htm
tech.root: winrt
ms.assetid: 68147308-65e9-4c19-e25a-f560ba96fc9c
ms.date: 12/05/2018
ms.keywords: CreateCompositionSurfaceForHandle, CreateCompositionSurfaceForHandle method, CreateCompositionSurfaceForHandle method,ICompositorInterop interface, ICompositorInterop interface,CreateCompositionSurfaceForHandle method, ICompositorInterop.CreateCompositionSurfaceForHandle, ICompositorInterop.composition, ICompositorInterop::CreateCompositionSurfaceForHandle, ICompositorInterop::composition, w_ui_comp.icompositorinterop_createcompositionsurfaceforhandle, windows/ICompositorInterop::CreateCompositionSurfaceForHandle
req.header: windows.ui.composition.interop.h
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
 - ICompositorInterop::CreateCompositionSurfaceForHandle
 - windows.ui.composition.interop/ICompositorInterop::CreateCompositionSurfaceForHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositorInterop.CreateCompositionSurfaceForHandle
---

# ICompositorInterop::CreateCompositionSurfaceForHandle (windows.ui.composition.interop.h)


## -description

Creates an instance of CompositionSurface for use with the handle of a swapchain. In order to host media swapchain on a CompositionSurface, use the IMFMediaEngineEx::GetVideoSwapchainHandle method.

## -parameters

### -param swapChain [in]

Type: <b>HANDLE*</b>

The handle of the swap chain to create the CompositionSurface for.

### -param result [out]

Type: <b>ICompositionSurface**</b>

The created CompositionSurface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositorinterop">ICompositorInterop</a>
