---
UID: NF:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded
title: IVirtualSurfaceImageSourceNative::xaml (windows.ui.xaml.media.dxinterop.h)
author: windows-sdk-content
description: Registers for the callback that will perform the drawing when an update to the shared surface is requested.
old-location: winrt\ivirtualsurfaceimagesourcenative_registerforupdatesneeded.htm
tech.root: WinRT
ms.assetid: D12AE5FD-ED3D-49E5-8E41-B1598C64A108
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IVirtualSurfaceImageSourceNative interface [Windows Runtime],RegisterForUpdatesNeeded method, IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded, IVirtualSurfaceImageSourceNative.xaml, IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded, IVirtualSurfaceImageSourceNative::xaml, RegisterForUpdatesNeeded, RegisterForUpdatesNeeded method [Windows Runtime], RegisterForUpdatesNeeded method [Windows Runtime],IVirtualSurfaceImageSourceNative interface, windows/IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded, winrt.ivirtualsurfaceimagesourcenative_registerforupdatesneeded
ms.topic: method
f1_keywords: ["windows.ui.xaml.media.dxinterop/IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVirtualSurfaceImageSourceNative::xaml


## -description


Registers for the callback that will perform the drawing when an update to the shared surface is requested.


## -parameters




### -param callback [in]

Pointer to an implementation of <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative">IVirtualSurfaceUpdatesCallbackNative</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative">IVirtualSurfaceUpdatesCallbackNative</a>
 

 

