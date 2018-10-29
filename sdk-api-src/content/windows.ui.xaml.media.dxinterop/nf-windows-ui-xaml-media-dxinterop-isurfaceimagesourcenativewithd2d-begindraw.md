---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D.BeginDraw
title: ISurfaceImageSourceNativeWithD2D::xaml
author: windows-sdk-content
description: Initiates an update to the associated SurfaceImageSource or VirtualSurfaceImageSource.
old-location: winrt\isurfaceimagesourcenativewithd2d_begindraw.htm
tech.root: WinRT
ms.assetid: 077458AB-7644-4973-8955-95E097DAF859
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: BeginDraw, BeginDraw method [Windows Runtime], BeginDraw method [Windows Runtime],ISurfaceImageSourceNativeWithD2D interface, ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],BeginDraw method, ISurfaceImageSourceNativeWithD2D.BeginDraw, ISurfaceImageSourceNativeWithD2D.xaml, ISurfaceImageSourceNativeWithD2D::BeginDraw, ISurfaceImageSourceNativeWithD2D::xaml, windows/ISurfaceImageSourceNativeWithD2D::BeginDraw, winrt.isurfaceimagesourcenativewithd2d_begindraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISurfaceImageSourceNativeWithD2D.BeginDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISurfaceImageSourceNativeWithD2D::xaml


## -description


Initiates an update to the associated <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> or <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>.


## -parameters




### -param updateRect [in]

The region of the surface that will be drawn into.


### -param iid [in]

IID used to lookup the object for drawing.


### -param updateObject [out]

Receives a COM pointer to the drawing object. Based on <i>iid</i>, this may be either an <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">IDXGISurface</a>, when not using batched drawing, or a shared <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>, when using batched Direct2D drawing to improve performance when updating Direct2D content across multiple surfaces. 


### -param offset [out]

Receives the point (x,y) offset of the surface that will be drawn into.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/5C004E4F-12C6-4C2E-AE9A-D841411FF689">ISurfaceImageSourceNativeWithD2D</a>



<a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a>



<a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>
 

 

