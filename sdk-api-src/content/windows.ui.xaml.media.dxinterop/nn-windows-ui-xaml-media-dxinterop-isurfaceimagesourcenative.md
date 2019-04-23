---
UID: NN:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNative
title: ISurfaceImageSourceNative (windows.ui.xaml.media.dxinterop.h)
author: windows-sdk-content
description: Provides the implementation of a shared fixed-size surface for Direct2D drawing.
old-location: winrt\isurfaceimagesourcenative.htm
tech.root: WinRT
ms.assetid: 55122048-FA3B-494F-8BD3-97D2C36E4579
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNative, ISurfaceImageSourceNative interface [Windows Runtime], ISurfaceImageSourceNative interface [Windows Runtime],described, windows/ISurfaceImageSourceNative, winrt.isurfaceimagesourcenative
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
 - ISurfaceImageSourceNative
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISurfaceImageSourceNative interface


## -description


Provides the implementation of a shared fixed-size surface for Direct2D drawing.
<div class="alert"><b>Note</b>  If the surface is larger than the screen size, use <a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">IVirtualSurfaceImageSourceNative</a> instead.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurfaceImageSourceNative</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISurfaceImageSourceNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurfaceImageSourceNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9F08AF78-AD8B-4AFC-ABFF-7006873FA506">BeginDraw</a>
</td>
<td align="left" width="63%">
Opens the supplied DXGI surface for drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/144EB343-DBBD-4E7E-8E05-87A35F4A5A64">EndDraw</a>
</td>
<td align="left" width="63%">
Closes the surface draw operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24DF51D3-3438-4AB4-BCA9-D5E2051B3CEA">SetDevice</a>
</td>
<td align="left" width="63%">
Sets the DXGI device, created with D3D11_CREATE_DEVICE_BGRA_SUPPORT, that will draw the surface.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> Windows runtime type. To obtain a pointer to <b>ISurfaceImageSourceNative</b>, you must cast a <b>SurfaceImageSource</b> instance to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<ISurfaceImageSourceNative>	m_sisNative;
// ...
IInspectable* sisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(surfaceImageSource);
sisInspectable->QueryInterface(__uuidof(ISurfaceImageSourceNative), (void **)&m_sisNative)
	
```





## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">IVirtualSurfaceImageSourceNative</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>
 

 

