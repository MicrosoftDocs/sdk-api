---
UID: NN:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNative
title: ISurfaceImageSourceNative (windows.ui.xaml.media.dxinterop.h)
description: Provides the implementation of a shared fixed-size surface for Direct2D drawing.
old-location: winrt\isurfaceimagesourcenative.htm
tech.root: WinRT
ms.assetid: 55122048-FA3B-494F-8BD3-97D2C36E4579
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNative, ISurfaceImageSourceNative interface [Windows Runtime], ISurfaceImageSourceNative interface [Windows Runtime],described, windows/ISurfaceImageSourceNative, winrt.isurfaceimagesourcenative
ms.topic: interface
f1_keywords:
- windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNative
dev_langs:
- c++
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.media.dxinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windows.UI.Xaml.dll
api_name:
- ISurfaceImageSourceNative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISurfaceImageSourceNative interface


## -description


Provides the implementation of a shared fixed-size surface for Direct2D drawing.
<div class="alert"><b>Note</b>  If the surface is larger than the screen size, use <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurfaceImageSourceNative</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISurfaceImageSourceNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurfaceImageSourceNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative-begindraw">BeginDraw</a>
</td>
<td align="left" width="63%">
Opens the supplied DXGI surface for drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative-enddraw">EndDraw</a>
</td>
<td align="left" width="63%">
Closes the surface draw operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative-setdevice">SetDevice</a>
</td>
<td align="left" width="63%">
Sets the DXGI device, created with D3D11_CREATE_DEVICE_BGRA_SUPPORT, that will draw the surface.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> Windows runtime type. To obtain a pointer to <b>ISurfaceImageSourceNative</b>, you must cast a <b>SurfaceImageSource</b> instance to <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISurfaceImageSourceNative>	m_sisNative;
// ...
IInspectable* sisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(surfaceImageSource);
sisInspectable->QueryInterface(__uuidof(ISurfaceImageSourceNative), (void **)&m_sisNative)
	
```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>
 

 

