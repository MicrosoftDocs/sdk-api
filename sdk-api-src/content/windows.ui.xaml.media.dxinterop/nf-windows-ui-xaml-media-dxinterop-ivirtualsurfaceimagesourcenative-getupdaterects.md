---
UID: NF:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative.GetUpdateRects
title: IVirtualSurfaceImageSourceNative::GetUpdateRects (windows.ui.xaml.media.dxinterop.h)
description: Gets the set of regions that must be updated on the shared surface.
helpviewer_keywords: ["GetUpdateRects","GetUpdateRects method [Windows Runtime]","GetUpdateRects method [Windows Runtime]","IVirtualSurfaceImageSourceNative interface","IVirtualSurfaceImageSourceNative interface [Windows Runtime]","GetUpdateRects method","IVirtualSurfaceImageSourceNative.GetUpdateRects","IVirtualSurfaceImageSourceNative.xaml","IVirtualSurfaceImageSourceNative::GetUpdateRects","IVirtualSurfaceImageSourceNative::xaml","windows/IVirtualSurfaceImageSourceNative::GetUpdateRects","winrt.ivirtualsurfaceimagesourcenative_getupdaterects"]
old-location: winrt\ivirtualsurfaceimagesourcenative_getupdaterects.htm
tech.root: WinRT
ms.assetid: C23F3F82-FB3B-4893-8C14-FC7D3C61D295
ms.date: 12/05/2018
ms.keywords: GetUpdateRects, GetUpdateRects method [Windows Runtime], GetUpdateRects method [Windows Runtime],IVirtualSurfaceImageSourceNative interface, IVirtualSurfaceImageSourceNative interface [Windows Runtime],GetUpdateRects method, IVirtualSurfaceImageSourceNative.GetUpdateRects, IVirtualSurfaceImageSourceNative.xaml, IVirtualSurfaceImageSourceNative::GetUpdateRects, IVirtualSurfaceImageSourceNative::xaml, windows/IVirtualSurfaceImageSourceNative::GetUpdateRects, winrt.ivirtualsurfaceimagesourcenative_getupdaterects
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
 - IVirtualSurfaceImageSourceNative::GetUpdateRects
 - windows.ui.xaml.media.dxinterop/IVirtualSurfaceImageSourceNative::GetUpdateRects
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
 - IVirtualSurfaceImageSourceNative.GetUpdateRects
---

# IVirtualSurfaceImageSourceNative::GetUpdateRects (windows.ui.xaml.media.dxinterop.h)


## -description

Gets the set of regions that must be updated on the shared surface.

## -parameters

### -param updates [in]

The number of regions that must be updated. You obtain this by calling <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-getupdaterectcount">GetUpdateRectCount</a>.

### -param count [out]

Receives a list of regions that must be updated.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a>
