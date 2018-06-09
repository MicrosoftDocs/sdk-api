---
UID: NF:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D.EndDraw
title: ISurfaceImageSourceNativeWithD2D::xaml
author: windows-sdk-content
description: Closes the surface draw operation.
old-location: winrt\isurfaceimagesourcenativewithd2d_enddraw.htm
old-project: WinRT
ms.assetid: 1E152D80-2673-43C6-B242-F89C890EE688
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: EndDraw, EndDraw method [Windows Runtime], EndDraw method [Windows Runtime],ISurfaceImageSourceNativeWithD2D interface, ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],EndDraw method, ISurfaceImageSourceNativeWithD2D.EndDraw, ISurfaceImageSourceNativeWithD2D.xaml, ISurfaceImageSourceNativeWithD2D::EndDraw, ISurfaceImageSourceNativeWithD2D::xaml, windows/ISurfaceImageSourceNativeWithD2D::EndDraw, winrt.isurfaceimagesourcenativewithd2d_enddraw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: windows.ui.xaml.media.dxinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.ui.xaml.media.dxinterop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISurfaceImageSourceNativeWithD2D.EndDraw
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
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




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/5C004E4F-12C6-4C2E-AE9A-D841411FF689">ISurfaceImageSourceNativeWithD2D</a>



<a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a>



<a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>
 

 

