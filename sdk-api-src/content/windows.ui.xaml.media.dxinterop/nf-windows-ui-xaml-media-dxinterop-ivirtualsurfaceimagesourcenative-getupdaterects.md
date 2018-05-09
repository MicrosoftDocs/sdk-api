---
UID: NF:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative.GetUpdateRects
title: IVirtualSurfaceImageSourceNative::xaml
author: windows-driver-content
description: Gets the set of regions that must be updated on the shared surface.
old-location: winrt\ivirtualsurfaceimagesourcenative_getupdaterects.htm
old-project: WinRT
ms.assetid: C23F3F82-FB3B-4893-8C14-FC7D3C61D295
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetUpdateRects, GetUpdateRects method [Windows Runtime], GetUpdateRects method [Windows Runtime],IVirtualSurfaceImageSourceNative interface, IVirtualSurfaceImageSourceNative interface [Windows Runtime],GetUpdateRects method, IVirtualSurfaceImageSourceNative.GetUpdateRects, IVirtualSurfaceImageSourceNative.xaml, IVirtualSurfaceImageSourceNative::GetUpdateRects, IVirtualSurfaceImageSourceNative::xaml, windows/IVirtualSurfaceImageSourceNative::GetUpdateRects, winrt.ivirtualsurfaceimagesourcenative_getupdaterects
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
-	IVirtualSurfaceImageSourceNative.GetUpdateRects
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IVirtualSurfaceImageSourceNative::xaml


## -description


Gets the set of regions that must be updated on the shared surface.


## -parameters




### -param updates




### -param count [in]

The number of regions that must be updated. You obtain this by calling <a href="https://msdn.microsoft.com/AE717587-0156-4DEC-B7B2-FF8937117D5A">GetUpdateRectCount</a>.


#### - pUpdates [out]

Receives a list of regions that must be updated.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">IVirtualSurfaceImageSourceNative</a>
 

 

