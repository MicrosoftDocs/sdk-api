---
UID: NN:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNative
title: ISurfaceImageSourceNative (windows.ui.xaml.media.dxinterop.h)
description: Provides the implementation of a shared fixed-size surface for Direct2D drawing.
helpviewer_keywords: ["ISurfaceImageSourceNative","ISurfaceImageSourceNative interface [Windows Runtime]","ISurfaceImageSourceNative interface [Windows Runtime]","described","windows/ISurfaceImageSourceNative","winrt.isurfaceimagesourcenative"]
old-location: winrt\isurfaceimagesourcenative.htm
tech.root: WinRT
ms.assetid: 55122048-FA3B-494F-8BD3-97D2C36E4579
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNative, ISurfaceImageSourceNative interface [Windows Runtime], ISurfaceImageSourceNative interface [Windows Runtime],described, windows/ISurfaceImageSourceNative, winrt.isurfaceimagesourcenative
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISurfaceImageSourceNative
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISurfaceImageSourceNative
---

# ISurfaceImageSourceNative interface


## -description

Provides the implementation of a shared fixed-size surface for Direct2D drawing.
<div class="alert"><b>Note</b>  If the surface is larger than the screen size, use <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a> instead.</div><div> </div>

## -inheritance

The <b>ISurfaceImageSourceNative</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISurfaceImageSourceNative</b> also has these types of members:

## -remarks

This interface provides the native implementation of the <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> Windows runtime type. To obtain a pointer to <b>ISurfaceImageSourceNative</b>, you must cast a <b>SurfaceImageSource</b> instance to <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISurfaceImageSourceNative>	m_sisNative;
// ...
IInspectable* sisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(surfaceImageSource);
sisInspectable->QueryInterface(__uuidof(ISurfaceImageSourceNative), (void **)&m_sisNative)
	
```

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>
