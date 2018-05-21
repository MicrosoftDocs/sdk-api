---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNative.BeginDraw
title: ISurfaceImageSourceNative::xaml
author: windows-driver-content
description: Opens the supplied DXGI surface for drawing.
old-location: winrt\isurfaceimagesourcenative_begindraw.htm
old-project: WinRT
ms.assetid: 9F08AF78-AD8B-4AFC-ABFF-7006873FA506
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: BeginDraw, BeginDraw method [Windows Runtime], BeginDraw method [Windows Runtime],ISurfaceImageSourceNative interface, ISurfaceImageSourceNative interface [Windows Runtime],BeginDraw method, ISurfaceImageSourceNative.BeginDraw, ISurfaceImageSourceNative.xaml, ISurfaceImageSourceNative::BeginDraw, ISurfaceImageSourceNative::xaml, windows/ISurfaceImageSourceNative::BeginDraw, winrt.isurfaceimagesourcenative_begindraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: PDF_RENDER_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windows.UI.Xaml.dll
api_name:
-	ISurfaceImageSourceNative.BeginDraw
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISurfaceImageSourceNative::xaml


## -description


Opens the supplied DXGI surface for drawing.


## -parameters




### -param updateRect [in]

The region of the surface that will be drawn into.


### -param surface




### -param offset [out]

Receives the point (x,y) offset of the surface that will be drawn into.


#### - pSurface [out]

Receives a pointer to the surface for drawing. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the app window that contains the <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> isn't active, like when it's suspended, calling the <b>BeginDraw</b> method returns an error.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">IDXGISurface</a>



<a href="https://msdn.microsoft.com/55122048-FA3B-494F-8BD3-97D2C36E4579">ISurfaceImageSourceNative</a>
 

 

