---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice
title: ISurfaceImageSourceManagerNative::xaml (windows.ui.xaml.media.dxinterop.h)
description: Flushes all current GPU work for all SurfaceImageSource or VirtualSurfaceImageSource objects associated with the given device.
helpviewer_keywords: ["FlushAllSurfacesWithDevice","FlushAllSurfacesWithDevice method [Windows Runtime]","FlushAllSurfacesWithDevice method [Windows Runtime]","ISurfaceImageSourceManagerNative interface","ISurfaceImageSourceManagerNative interface [Windows Runtime]","FlushAllSurfacesWithDevice method","ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice","ISurfaceImageSourceManagerNative.xaml","ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice","ISurfaceImageSourceManagerNative::xaml","windows/ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice","winrt.isurfaceimagesourcemanagernative_flushallsurfaceswithdevice"]
old-location: winrt\isurfaceimagesourcemanagernative_flushallsurfaceswithdevice.htm
tech.root: WinRT
ms.assetid: 2921FF9E-25C5-4DF6-B23F-7B60F0577983
ms.date: 12/05/2018
ms.keywords: FlushAllSurfacesWithDevice, FlushAllSurfacesWithDevice method [Windows Runtime], FlushAllSurfacesWithDevice method [Windows Runtime],ISurfaceImageSourceManagerNative interface, ISurfaceImageSourceManagerNative interface [Windows Runtime],FlushAllSurfacesWithDevice method, ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice, ISurfaceImageSourceManagerNative.xaml, ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice, ISurfaceImageSourceManagerNative::xaml, windows/ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice, winrt.isurfaceimagesourcemanagernative_flushallsurfaceswithdevice
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
 - ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceManagerNative::FlushAllSurfacesWithDevice
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
 - ISurfaceImageSourceManagerNative.FlushAllSurfacesWithDevice
---

# ISurfaceImageSourceManagerNative::xaml


## -description

Flushes all current GPU work for all <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> or <a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>  objects associated with the given device.

## -parameters

### -param device [in]

The device that was used to create <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> objects in this process.  It must be an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> or an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>FlushAllSurfacesWithDevice</b> method flushes current GPU work for all <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> objects that were created with <i>device</i>.  This GPU work includes Direct2D rendering work and internal GPU work done by the framework associated with rendering.  This is useful if an application has created multiple <b>SurfaceImageSource</b> objects and needs to flush the GPU work for all of these surfaces from the background rendering thread.  By flushing this work from the background thread the work can be better parallelized, with work being done on the UI thread to improve performance.

You can call the <b>FlushAllSurfacesWithDevice</b> method from a non-UI thread.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative">ISurfaceImageSourceManagerNative</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>