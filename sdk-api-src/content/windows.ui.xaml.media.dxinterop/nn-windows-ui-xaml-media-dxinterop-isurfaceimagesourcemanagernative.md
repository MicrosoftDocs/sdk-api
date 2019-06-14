---
UID: NN:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceManagerNative
title: ISurfaceImageSourceManagerNative (windows.ui.xaml.media.dxinterop.h)
author: windows-sdk-content
description: Enables performing bulk operations across all SurfaceImageSource objects created in the same process.
old-location: winrt\isurfaceimagesourcemanagernative.htm
tech.root: WinRT
ms.assetid: 6DFC7A3D-0C29-421B-ADB0-360017DE7433
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceManagerNative, ISurfaceImageSourceManagerNative interface [Windows Runtime], ISurfaceImageSourceManagerNative interface [Windows Runtime],described, windows/ISurfaceImageSourceManagerNative, winrt.isurfaceimagesourcemanagernative
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
 - ISurfaceImageSourceManagerNative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISurfaceImageSourceManagerNative interface


## -description


Enables performing bulk operations across all <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> objects created in the same process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurfaceImageSourceManagerNative</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISurfaceImageSourceManagerNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurfaceImageSourceManagerNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative-flushallsurfaceswithdevice">FlushAllSurfacesWithDevice</a>
</td>
<td align="left" width="63%">
Flushes all current GPU work for all <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> or <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>  objects associated with the given device.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>
 

 

