---
UID: NN:windows.ui.composition.interop.ICompositionGraphicsDeviceInterop
title: ICompositionGraphicsDeviceInterop (windows.ui.composition.interop.h)
description: A native interoperation interface that allows getting and setting the graphics device. This is interface is available in C++ only.
helpviewer_keywords: ["ICompositionGraphicsDeviceInterop","ICompositionGraphicsDeviceInterop interface","ICompositionGraphicsDeviceInterop interface","described","w_ui_comp.icompositiongraphicsdeviceinterop","windows/ICompositionGraphicsDeviceInterop"]
old-location: w_ui_comp\icompositiongraphicsdeviceinterop.htm
tech.root: winrt
ms.assetid: E8585E49-DB1E-44CA-AE75-138E87FD2D30
ms.date: 12/05/2018
ms.keywords: ICompositionGraphicsDeviceInterop, ICompositionGraphicsDeviceInterop interface, ICompositionGraphicsDeviceInterop interface,described, w_ui_comp.icompositiongraphicsdeviceinterop, windows/ICompositionGraphicsDeviceInterop
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
 - ICompositionGraphicsDeviceInterop
 - windows.ui.composition.interop/ICompositionGraphicsDeviceInterop
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
 - ICompositionGraphicsDeviceInterop
---

# ICompositionGraphicsDeviceInterop interface


## -description

A native interoperation  interface that allows getting and setting the graphics device.
          This is interface is available in C++ only.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICompositionGraphicsDeviceInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICompositionGraphicsDeviceInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICompositionGraphicsDeviceInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiongraphicsdeviceinterop-getrenderingdevice">GetRenderingDevice</a>
</td>
<td align="left" width="63%">
Gets the rendering device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nf-windows-ui-composition-interop-icompositiongraphicsdeviceinterop-setrenderingdevice">SetRenderingDevice</a>
</td>
<td align="left" width="63%">
Sets the rendering device.

</td>
</tr>
</table>

## -remarks

See <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop">ICompositionDrawingSurfaceInterop</a> for usage examples.

## -see-also

<a href="https://docs.microsoft.com/windows/uwp/composition/composition-native-interop">Composition Native Interoperation Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

