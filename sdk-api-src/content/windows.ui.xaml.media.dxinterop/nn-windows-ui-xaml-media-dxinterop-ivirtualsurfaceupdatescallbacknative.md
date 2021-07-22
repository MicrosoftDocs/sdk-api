---
UID: NN:windows.ui.xaml.media.dxinterop.IVirtualSurfaceUpdatesCallbackNative
title: IVirtualSurfaceUpdatesCallbackNative (windows.ui.xaml.media.dxinterop.h)
description: Provides an interface for the implementation of drawing behaviors when a VirtualSurfaceImageSource requests an update.
helpviewer_keywords: ["IVirtualSurfaceUpdatesCallbackNative","IVirtualSurfaceUpdatesCallbackNative interface [Windows Runtime]","IVirtualSurfaceUpdatesCallbackNative interface [Windows Runtime]","described","windows/IVirtualSurfaceUpdatesCallbackNative","winrt.ivirtualsurfaceupdatescallbacknative"]
old-location: winrt\ivirtualsurfaceupdatescallbacknative.htm
tech.root: WinRT
ms.assetid: 76B5E0B6-7DE4-41A4-B33B-2C6A32D47DB1
ms.date: 12/05/2018
ms.keywords: IVirtualSurfaceUpdatesCallbackNative, IVirtualSurfaceUpdatesCallbackNative interface [Windows Runtime], IVirtualSurfaceUpdatesCallbackNative interface [Windows Runtime],described, windows/IVirtualSurfaceUpdatesCallbackNative, winrt.ivirtualsurfaceupdatescallbacknative
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
 - IVirtualSurfaceUpdatesCallbackNative
 - windows.ui.xaml.media.dxinterop/IVirtualSurfaceUpdatesCallbackNative
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
 - IVirtualSurfaceUpdatesCallbackNative
---

# IVirtualSurfaceUpdatesCallbackNative interface


## -description

Provides an interface for the implementation of drawing behaviors when a <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">VirtualSurfaceImageSource</a> requests an update.

## -inheritance

The <b>IVirtualSurfaceUpdatesCallbackNative</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVirtualSurfaceUpdatesCallbackNative</b> also has these types of members:

## -remarks

This interface is implemented by the developer to provide specific drawing behaviors for updates to a <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">VirtualSurfaceImageSource</a>. Classes that implement  this interface are provided to the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-registerforupdatesneeded">IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded</a>, which calls the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative-updatesneeded">UpdatesNeeded</a> method implementation whenever an update is requested.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<b>IVirtualSurfaceImageSourceNative</b>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-registerforupdatesneeded">IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">VirtualSurfaceImageSource</a>
