---
UID: NF:windows.ui.composition.interop.ICompositorInterop.CreateCompositionSurfaceForSwapChain
title: ICompositorInterop::CreateCompositionSurfaceForSwapChain (windows.ui.composition.interop.h)
description: Creates an instance of CompositionSurface for use with a swap chain.
helpviewer_keywords: ["CreateCompositionSurfaceForSwapChain","CreateCompositionSurfaceForSwapChain method","CreateCompositionSurfaceForSwapChain method","ICompositorInterop interface","ICompositorInterop interface","CreateCompositionSurfaceForSwapChain method","ICompositorInterop.CreateCompositionSurfaceForSwapChain","ICompositorInterop.composition","ICompositorInterop::CreateCompositionSurfaceForSwapChain","ICompositorInterop::composition","w_ui_comp.icompositorinterop_createcompositionsurfaceforswapchain","windows/ICompositorInterop::CreateCompositionSurfaceForSwapChain"]
old-location: w_ui_comp\icompositorinterop_createcompositionsurfaceforswapchain.htm
tech.root: winrt
ms.assetid: FDF81740-C6BA-4F3D-8145-749C738718E5
ms.date: 12/05/2018
ms.keywords: CreateCompositionSurfaceForSwapChain, CreateCompositionSurfaceForSwapChain method, CreateCompositionSurfaceForSwapChain method,ICompositorInterop interface, ICompositorInterop interface,CreateCompositionSurfaceForSwapChain method, ICompositorInterop.CreateCompositionSurfaceForSwapChain, ICompositorInterop.composition, ICompositorInterop::CreateCompositionSurfaceForSwapChain, ICompositorInterop::composition, w_ui_comp.icompositorinterop_createcompositionsurfaceforswapchain, windows/ICompositorInterop::CreateCompositionSurfaceForSwapChain
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
 - ICompositorInterop::CreateCompositionSurfaceForSwapChain
 - windows.ui.composition.interop/ICompositorInterop::CreateCompositionSurfaceForSwapChain
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
 - ICompositorInterop.CreateCompositionSurfaceForSwapChain
---

# ICompositorInterop::CreateCompositionSurfaceForSwapChain (windows.ui.composition.interop.h)


## -description

Creates an instance of CompositionSurface for use with a swap chain.

## -parameters

### -param swapChain [in]

Type: <b>IUnknown*</b>

The swap chain to create the CompositionSurface for.

### -param result [out]

Type: <b>ICompositionSurface**</b>

The created CompositionSurface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -see-also

<a href="/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositorinterop">ICompositorInterop</a>
