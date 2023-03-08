---
UID: NN:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative
title: IVirtualSurfaceImageSourceNative (windows.ui.xaml.media.dxinterop.h)
description: Provides the implementation of a large (greater than the screen size) shared surface for DirectX drawing.
helpviewer_keywords: ["IVirtualSurfaceImageSourceNative","IVirtualSurfaceImageSourceNative interface [Windows Runtime]","IVirtualSurfaceImageSourceNative interface [Windows Runtime]","described","windows/IVirtualSurfaceImageSourceNative","winrt.ivirtualsurfaceimagesourcenative"]
old-location: winrt\ivirtualsurfaceimagesourcenative.htm
tech.root: WinRT
ms.assetid: 1CABA8F5-2380-45B9-804C-B1DC9FF34B62
ms.date: 12/05/2018
ms.keywords: IVirtualSurfaceImageSourceNative, IVirtualSurfaceImageSourceNative interface [Windows Runtime], IVirtualSurfaceImageSourceNative interface [Windows Runtime],described, windows/IVirtualSurfaceImageSourceNative, winrt.ivirtualsurfaceimagesourcenative
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
 - IVirtualSurfaceImageSourceNative
 - windows.ui.xaml.media.dxinterop/IVirtualSurfaceImageSourceNative
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
 - IVirtualSurfaceImageSourceNative
---

# IVirtualSurfaceImageSourceNative interface


## -description

Provides the implementation of a large (greater than the screen size) shared surface for DirectX drawing.

## -inheritance

The <b>IVirtualSurfaceImageSourceNative</b> interface inherits from <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a>. <b>IVirtualSurfaceImageSourceNative</b> also has these types of members:

## -remarks

This interface provides the native implementation of the <a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">Windows::UI::Xaml::Media::Imaging::VirtualSurfaceImageSource</a> Windows runtime type. To obtain a pointer to <b>IVirtualSurfaceImageSourceNative</b>, you must cast a <b>VirtualSurfaceImageSource</b> instance to <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<IVirtualSurfaceImageSourceNative>	m_vsisNative;
// ...
IInspectable* vsisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(virtualSurfaceImageSource);
vsisInspectable->QueryInterface(__uuidof(IVirtualSurfaceImageSourceNative), (void **)&m_vsisNative)
	
```

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a>
