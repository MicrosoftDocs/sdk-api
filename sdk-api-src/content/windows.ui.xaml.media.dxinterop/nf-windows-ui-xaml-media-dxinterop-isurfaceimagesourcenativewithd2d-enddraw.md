---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D.EndDraw
title: ISurfaceImageSourceNativeWithD2D::xaml (windows.ui.xaml.media.dxinterop.h)
description: Closes the surface draw operation.
helpviewer_keywords: ["EndDraw","EndDraw method [Windows Runtime]","EndDraw method [Windows Runtime]","ISurfaceImageSourceNativeWithD2D interface","ISurfaceImageSourceNativeWithD2D interface [Windows Runtime]","EndDraw method","ISurfaceImageSourceNativeWithD2D.EndDraw","ISurfaceImageSourceNativeWithD2D.xaml","ISurfaceImageSourceNativeWithD2D::EndDraw","ISurfaceImageSourceNativeWithD2D::xaml","windows/ISurfaceImageSourceNativeWithD2D::EndDraw","winrt.isurfaceimagesourcenativewithd2d_enddraw"]
old-location: winrt\isurfaceimagesourcenativewithd2d_enddraw.htm
tech.root: WinRT
ms.assetid: 1E152D80-2673-43C6-B242-F89C890EE688
ms.date: 12/05/2018
ms.keywords: EndDraw, EndDraw method [Windows Runtime], EndDraw method [Windows Runtime],ISurfaceImageSourceNativeWithD2D interface, ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],EndDraw method, ISurfaceImageSourceNativeWithD2D.EndDraw, ISurfaceImageSourceNativeWithD2D.xaml, ISurfaceImageSourceNativeWithD2D::EndDraw, ISurfaceImageSourceNativeWithD2D::xaml, windows/ISurfaceImageSourceNativeWithD2D::EndDraw, winrt.isurfaceimagesourcenativewithd2d_enddraw
f1_keywords:
- windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNativeWithD2D.EndDraw
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Windows.UI.Xaml.dll
api_name:
- ISurfaceImageSourceNativeWithD2D.EndDraw
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISurfaceImageSourceNativeWithD2D::xaml


## -description


Closes the surface draw operation.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Always call the <b>EndDraw</b> method on the UI thread in order to synchronize updating the Microsoft DirectX content with the current XAML UI thread frame.  




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d">ISurfaceImageSourceNativeWithD2D</a>



<a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>



<a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>
 

 

