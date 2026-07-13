---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D.BeginDraw
title: ISurfaceImageSourceNativeWithD2D::BeginDraw (windows.ui.xaml.media.dxinterop.h)
description: Initiates an update to the associated SurfaceImageSource or VirtualSurfaceImageSource.
helpviewer_keywords: ["BeginDraw","BeginDraw method [Windows Runtime]","BeginDraw method [Windows Runtime]","ISurfaceImageSourceNativeWithD2D interface","ISurfaceImageSourceNativeWithD2D interface [Windows Runtime]","BeginDraw method","ISurfaceImageSourceNativeWithD2D.BeginDraw","ISurfaceImageSourceNativeWithD2D.xaml","ISurfaceImageSourceNativeWithD2D::BeginDraw","ISurfaceImageSourceNativeWithD2D::xaml","windows/ISurfaceImageSourceNativeWithD2D::BeginDraw","winrt.isurfaceimagesourcenativewithd2d_begindraw"]
old-location: winrt\isurfaceimagesourcenativewithd2d_begindraw.htm
tech.root: WinRT
ms.assetid: 077458AB-7644-4973-8955-95E097DAF859
ms.date: 12/05/2018
ms.keywords: BeginDraw, BeginDraw method [Windows Runtime], BeginDraw method [Windows Runtime],ISurfaceImageSourceNativeWithD2D interface, ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],BeginDraw method, ISurfaceImageSourceNativeWithD2D.BeginDraw, ISurfaceImageSourceNativeWithD2D.xaml, ISurfaceImageSourceNativeWithD2D::BeginDraw, ISurfaceImageSourceNativeWithD2D::xaml, windows/ISurfaceImageSourceNativeWithD2D::BeginDraw, winrt.isurfaceimagesourcenativewithd2d_begindraw
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
 - ISurfaceImageSourceNativeWithD2D::BeginDraw
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNativeWithD2D::BeginDraw
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
 - ISurfaceImageSourceNativeWithD2D.BeginDraw
---

# ISurfaceImageSourceNativeWithD2D::BeginDraw (windows.ui.xaml.media.dxinterop.h)


## -description

Initiates an update to the associated <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> or <a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>.

## -parameters

### -param updateRect [in]

The region of the surface that will be drawn into.

### -param iid [in]

IID used to lookup the object for drawing.

### -param updateObject [out]

Receives a COM pointer to the drawing object. Based on <i>iid</i>, this may be either an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>, when not using batched drawing, or a shared <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>, when using batched Direct2D drawing to improve performance when updating Direct2D content across multiple surfaces.

### -param offset [out]

Receives the point (x,y) offset of the surface that will be drawn into.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d">ISurfaceImageSourceNativeWithD2D</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>
