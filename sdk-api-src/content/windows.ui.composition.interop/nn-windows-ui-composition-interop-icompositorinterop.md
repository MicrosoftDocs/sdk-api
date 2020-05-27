---
UID: NN:windows.ui.composition.interop.ICompositorInterop
title: ICompositorInterop (windows.ui.composition.interop.h)
description: Native interoperation interface that allows creating swapchain surfaces and graphics devices. This is interface is available in C++ only.
helpviewer_keywords: ["ICompositorInterop","ICompositorInterop interface","ICompositorInterop interface","described","w_ui_comp.icompositorinterop","windows/ICompositorInterop"]
old-location: w_ui_comp\icompositorinterop.htm
tech.root: w_ui_comp
ms.assetid: 0BE505EA-1C31-411E-AAF7-06D52D9F4682
ms.date: 12/05/2018
ms.keywords: ICompositorInterop, ICompositorInterop interface, ICompositorInterop interface,described, w_ui_comp.icompositorinterop, windows/ICompositorInterop
f1_keywords:
- windows.ui.composition.interop/ICompositorInterop
dev_langs:
- c++
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
- ICompositorInterop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICompositorInterop interface


## -description


Native interoperation interface that allows creating swapchain surfaces and graphics devices. This is interface is available in C++ only.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICompositorInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICompositorInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICompositorInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositorinterop-createcompositionsurfaceforhandle">CreateCompositionSurfaceForHandle</a>
</td>
<td align="left" width="63%">
Creates an instance of CompositionSurface for use with the handle of a swapchain. In order to host media swapchain on a CompositionSurface, use the IMFMediaEngineEx::GetVideoSwapchainHandle method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositorinterop-createcompositionsurfaceforswapchain">CreateCompositionSurfaceForSwapChain</a>
</td>
<td align="left" width="63%">
Creates an instance of CompositionSurface for use with a swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositorinterop-creategraphicsdevice">CreateGraphicsDevice</a>
</td>
<td align="left" width="63%">
Creates a CompositionGraphicsDevice backed by the specified rendering device.

</td>
</tr>
</table> 


## -remarks



See <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop">ICompositionDrawingSurfaceInterop</a> for usage examples.




## -see-also




<a href="https://docs.microsoft.com/windows/uwp/composition/composition-native-interop">Composition Native Interoperation Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

