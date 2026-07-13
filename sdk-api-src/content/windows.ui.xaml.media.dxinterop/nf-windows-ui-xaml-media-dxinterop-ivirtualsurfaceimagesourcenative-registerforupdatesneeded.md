---
UID: NF:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded
title: IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded (windows.ui.xaml.media.dxinterop.h)
description: Registers for the callback that will perform the drawing when an update to the shared surface is requested.
helpviewer_keywords: ["IVirtualSurfaceImageSourceNative interface [Windows Runtime]","RegisterForUpdatesNeeded method","IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded","IVirtualSurfaceImageSourceNative.xaml","IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded","IVirtualSurfaceImageSourceNative::xaml","RegisterForUpdatesNeeded","RegisterForUpdatesNeeded method [Windows Runtime]","RegisterForUpdatesNeeded method [Windows Runtime]","IVirtualSurfaceImageSourceNative interface","windows/IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded","winrt.ivirtualsurfaceimagesourcenative_registerforupdatesneeded"]
old-location: winrt\ivirtualsurfaceimagesourcenative_registerforupdatesneeded.htm
tech.root: WinRT
ms.assetid: D12AE5FD-ED3D-49E5-8E41-B1598C64A108
ms.date: 12/05/2018
ms.keywords: IVirtualSurfaceImageSourceNative interface [Windows Runtime],RegisterForUpdatesNeeded method, IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded, IVirtualSurfaceImageSourceNative.xaml, IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded, IVirtualSurfaceImageSourceNative::xaml, RegisterForUpdatesNeeded, RegisterForUpdatesNeeded method [Windows Runtime], RegisterForUpdatesNeeded method [Windows Runtime],IVirtualSurfaceImageSourceNative interface, windows/IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded, winrt.ivirtualsurfaceimagesourcenative_registerforupdatesneeded
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
 - IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded
 - windows.ui.xaml.media.dxinterop/IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded
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
 - IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded
---

# IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded (windows.ui.xaml.media.dxinterop.h)


## -description

Registers for the callback that will perform the drawing when an update to the shared surface is requested.

## -parameters

### -param callback [in]

Pointer to an implementation of <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative">IVirtualSurfaceUpdatesCallbackNative</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative">IVirtualSurfaceUpdatesCallbackNative</a>
