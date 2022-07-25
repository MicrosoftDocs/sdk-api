---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNative.BeginDraw
title: ISurfaceImageSourceNative::BeginDraw (windows.ui.xaml.media.dxinterop.h)
description: Opens the supplied DXGI surface for drawing.
helpviewer_keywords: ["BeginDraw","BeginDraw method [Windows Runtime]","BeginDraw method [Windows Runtime]","ISurfaceImageSourceNative interface","ISurfaceImageSourceNative interface [Windows Runtime]","BeginDraw method","ISurfaceImageSourceNative.BeginDraw","ISurfaceImageSourceNative.xaml","ISurfaceImageSourceNative::BeginDraw","ISurfaceImageSourceNative::xaml","windows/ISurfaceImageSourceNative::BeginDraw","winrt.isurfaceimagesourcenative_begindraw"]
old-location: winrt\isurfaceimagesourcenative_begindraw.htm
tech.root: WinRT
ms.assetid: 9F08AF78-AD8B-4AFC-ABFF-7006873FA506
ms.date: 12/05/2018
ms.keywords: BeginDraw, BeginDraw method [Windows Runtime], BeginDraw method [Windows Runtime],ISurfaceImageSourceNative interface, ISurfaceImageSourceNative interface [Windows Runtime],BeginDraw method, ISurfaceImageSourceNative.BeginDraw, ISurfaceImageSourceNative.xaml, ISurfaceImageSourceNative::BeginDraw, ISurfaceImageSourceNative::xaml, windows/ISurfaceImageSourceNative::BeginDraw, winrt.isurfaceimagesourcenative_begindraw
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [UWP apps only]
req.target-min-winversvr: Windows Server 2012 R2 [UWP apps only]
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
 - ISurfaceImageSourceNative::BeginDraw
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNative::BeginDraw
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
 - ISurfaceImageSourceNative.BeginDraw
---

# ISurfaceImageSourceNative::BeginDraw (windows.ui.xaml.media.dxinterop.h)


## -description

Opens the supplied DXGI surface for drawing.

## -parameters

### -param updateRect [in]

The region of the surface that will be drawn into.

### -param surface [out]

Receives a pointer to the surface for drawing.

### -param offset [out]

Receives the point (x,y) offset of the surface that will be drawn into.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the app window that contains the <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> isn't active, like when it's suspended, calling the <b>BeginDraw</b> method returns an error.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a>
