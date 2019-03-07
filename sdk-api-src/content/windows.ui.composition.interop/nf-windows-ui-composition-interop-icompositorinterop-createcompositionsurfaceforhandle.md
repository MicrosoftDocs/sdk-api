---
UID: NF:windows.ui.composition.interop.ICompositorInterop.CreateCompositionSurfaceForHandle
title: ICompositorInterop::composition
author: windows-sdk-content
description: Creates an instance of CompositionSurface for use with the handle of a swapchain. In order to host media swapchain on a CompositionSurface, use the IMFMediaEngineEx::GetVideoSwapchainHandle method.
old-location: w_ui_comp\icompositorinterop_createcompositionsurfaceforhandle.htm
tech.root: w_ui_comp
ms.assetid: 68147308-65e9-4c19-e25a-f560ba96fc9c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateCompositionSurfaceForHandle, CreateCompositionSurfaceForHandle method, CreateCompositionSurfaceForHandle method,ICompositorInterop interface, ICompositorInterop interface,CreateCompositionSurfaceForHandle method, ICompositorInterop.CreateCompositionSurfaceForHandle, ICompositorInterop.composition, ICompositorInterop::CreateCompositionSurfaceForHandle, ICompositorInterop::composition, w_ui_comp.icompositorinterop_createcompositionsurfaceforhandle, windows/ICompositorInterop::CreateCompositionSurfaceForHandle
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositorInterop.CreateCompositionSurfaceForHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICompositorInterop::composition


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



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/0BE505EA-1C31-411E-AAF7-06D52D9F4682">ICompositorInterop</a>
 

 

