---
UID: NN:windows.ui.xaml.media.dxinterop.IVirtualSurfaceUpdatesCallbackNative
title: IVirtualSurfaceUpdatesCallbackNative
author: windows-sdk-content
description: Provides an interface for the implementation of drawing behaviors when a VirtualSurfaceImageSource requests an update.
old-location: winrt\ivirtualsurfaceupdatescallbacknative.htm
old-project: WinRT
ms.assetid: 76B5E0B6-7DE4-41A4-B33B-2C6A32D47DB1
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IVirtualSurfaceUpdatesCallbackNative, IVirtualSurfaceUpdatesCallbackNative interface [Windows Runtime], IVirtualSurfaceUpdatesCallbackNative interface [Windows Runtime],described, windows/IVirtualSurfaceUpdatesCallbackNative, winrt.ivirtualsurfaceupdatescallbacknative
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IVirtualSurfaceUpdatesCallbackNative
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IVirtualSurfaceUpdatesCallbackNative interface


## -description


Provides an interface for the implementation of drawing behaviors when a <a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">VirtualSurfaceImageSource</a> requests an update. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVirtualSurfaceUpdatesCallbackNative</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVirtualSurfaceUpdatesCallbackNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVirtualSurfaceUpdatesCallbackNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D689C977-3182-41FE-A789-8A349AC2FB10">UpdatesNeeded</a>
</td>
<td align="left" width="63%">
Performs the drawing behaviors when an update to <a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">VirtualSurfaceImageSource</a> is requested.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by the developer to provide specific drawing behaviors for updates to a <a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">VirtualSurfaceImageSource</a>. Classes that implement  this interface are provided to the <a href="https://msdn.microsoft.com/D12AE5FD-ED3D-49E5-8E41-B1598C64A108">IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded</a>, which calls the <a href="https://msdn.microsoft.com/D689C977-3182-41FE-A789-8A349AC2FB10">UpdatesNeeded</a> method implementation whenever an update is requested.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<b>IVirtualSurfaceImageSourceNative</b>



<a href="https://msdn.microsoft.com/D12AE5FD-ED3D-49E5-8E41-B1598C64A108">IVirtualSurfaceImageSourceNative::RegisterForUpdatesNeeded</a>



<a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">VirtualSurfaceImageSource</a>
 

 

