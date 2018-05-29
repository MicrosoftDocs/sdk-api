---
UID: NF:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded
title: IVirtualSurfaceImageSourceNative::xaml
author: windows-sdk-content
description: Registers for the callback that will perform the drawing when an update to the shared surface is requested.
old-location: winrt\ivirtualsurfaceimagesourcenative_registerforupdatesneeded.htm
old-project: WinRT
ms.assetid: D12AE5FD-ED3D-49E5-8E41-B1598C64A108
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: IVirtualSurfaceImageSourceNative interface [Windows Runtime],RegisterForUpdatesNeeded method, IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded, IVirtualSurfaceImageSourceNative.xaml, IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded, IVirtualSurfaceImageSourceNative::xaml, RegisterForUpdatesNeeded, RegisterForUpdatesNeeded method [Windows Runtime], RegisterForUpdatesNeeded method [Windows Runtime],IVirtualSurfaceImageSourceNative interface, windows/IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded, winrt.ivirtualsurfaceimagesourcenative_registerforupdatesneeded
ms.prod: windows
ms.technology: windows-sdk
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
-	IVirtualSurfaceImageSourceNative.RegisterForUpdatesNeeded
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IVirtualSurfaceImageSourceNative::xaml


## -description


Registers for the callback that will perform the drawing when an update to the shared surface is requested.


## -parameters




### -param callback






#### - pCallback [in]

Pointer to an implementation of <a href="https://msdn.microsoft.com/76B5E0B6-7DE4-41A4-B33B-2C6A32D47DB1">IVirtualSurfaceUpdatesCallbackNative</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">IVirtualSurfaceImageSourceNative</a>



<a href="https://msdn.microsoft.com/76B5E0B6-7DE4-41A4-B33B-2C6A32D47DB1">IVirtualSurfaceUpdatesCallbackNative</a>
 

 

