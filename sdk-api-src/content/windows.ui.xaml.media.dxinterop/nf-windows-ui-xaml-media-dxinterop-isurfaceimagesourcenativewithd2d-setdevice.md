---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D.SetDevice
title: ISurfaceImageSourceNativeWithD2D::SetDevice (windows.ui.xaml.media.dxinterop.h)
description: Sets the Microsoft DirectX Graphics Infrastructure (DXGI) or Direct2D device, created with D3D11_CREATE_DEVICE_BGRA_SUPPORT, that will draw the surface.
helpviewer_keywords: ["ISurfaceImageSourceNativeWithD2D interface [Windows Runtime]","SetDevice method","ISurfaceImageSourceNativeWithD2D.SetDevice","ISurfaceImageSourceNativeWithD2D.xaml","ISurfaceImageSourceNativeWithD2D::SetDevice","ISurfaceImageSourceNativeWithD2D::xaml","SetDevice","SetDevice method [Windows Runtime]","SetDevice method [Windows Runtime]","ISurfaceImageSourceNativeWithD2D interface","windows/ISurfaceImageSourceNativeWithD2D::SetDevice","winrt.isurfaceimagesourcenativewithd2d_setdevice"]
old-location: winrt\isurfaceimagesourcenativewithd2d_setdevice.htm
tech.root: WinRT
ms.assetid: FBBF0A5E-68FF-4143-A874-0C1100100428
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],SetDevice method, ISurfaceImageSourceNativeWithD2D.SetDevice, ISurfaceImageSourceNativeWithD2D.xaml, ISurfaceImageSourceNativeWithD2D::SetDevice, ISurfaceImageSourceNativeWithD2D::xaml, SetDevice, SetDevice method [Windows Runtime], SetDevice method [Windows Runtime],ISurfaceImageSourceNativeWithD2D interface, windows/ISurfaceImageSourceNativeWithD2D::SetDevice, winrt.isurfaceimagesourcenativewithd2d_setdevice
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
 - ISurfaceImageSourceNativeWithD2D::SetDevice
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNativeWithD2D::SetDevice
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
 - ISurfaceImageSourceNativeWithD2D.SetDevice
---

# ISurfaceImageSourceNativeWithD2D::SetDevice (windows.ui.xaml.media.dxinterop.h)


## -description

Sets the Microsoft DirectX Graphics Infrastructure (DXGI) or Direct2D device, created with <b>D3D11_CREATE_DEVICE_BGRA_SUPPORT</b>, that will draw the surface.

## -parameters

### -param device [in]

Pointer to the DXGI device interface. You can pass an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> to signal that this surface participates in Direct2D batching to improve performance when updating Direct2D content across multiple surfaces.  The device must have multithreading supported enabled if the app draws to the surface from a background thread.

## -returns

This method fails when the SurfaceImageSource is larger than the maximum texture size supported by the Direct3D device. Apps should use VirtualSurfaceImageSource for surfaces larger than the maximum texture size supported by the Direct3D device.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d">ISurfaceImageSourceNativeWithD2D</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>
