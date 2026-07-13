---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNative.SetDevice
title: ISurfaceImageSourceNative::SetDevice (windows.ui.xaml.media.dxinterop.h)
description: Sets the DXGI device, created with D3D11_CREATE_DEVICE_BGRA_SUPPORT, that will draw the surface.
helpviewer_keywords: ["ISurfaceImageSourceNative interface [Windows Runtime]","SetDevice method","ISurfaceImageSourceNative.SetDevice","ISurfaceImageSourceNative.xaml","ISurfaceImageSourceNative::SetDevice","ISurfaceImageSourceNative::xaml","SetDevice","SetDevice method [Windows Runtime]","SetDevice method [Windows Runtime]","ISurfaceImageSourceNative interface","windows/ISurfaceImageSourceNative::SetDevice","winrt.isurfaceimagesourcenative_setdevice"]
old-location: winrt\isurfaceimagesourcenative_setdevice.htm
tech.root: WinRT
ms.assetid: 24DF51D3-3438-4AB4-BCA9-D5E2051B3CEA
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNative interface [Windows Runtime],SetDevice method, ISurfaceImageSourceNative.SetDevice, ISurfaceImageSourceNative.xaml, ISurfaceImageSourceNative::SetDevice, ISurfaceImageSourceNative::xaml, SetDevice, SetDevice method [Windows Runtime], SetDevice method [Windows Runtime],ISurfaceImageSourceNative interface, windows/ISurfaceImageSourceNative::SetDevice, winrt.isurfaceimagesourcenative_setdevice
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
 - ISurfaceImageSourceNative::SetDevice
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNative::SetDevice
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
 - ISurfaceImageSourceNative.SetDevice
---

# ISurfaceImageSourceNative::SetDevice (windows.ui.xaml.media.dxinterop.h)


## -description

Sets the DXGI device, created with D3D11_CREATE_DEVICE_BGRA_SUPPORT, that will draw the surface.  This method must be called from the UI thread.

## -parameters

### -param device [in]

Pointer to the DXGI device interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a>
