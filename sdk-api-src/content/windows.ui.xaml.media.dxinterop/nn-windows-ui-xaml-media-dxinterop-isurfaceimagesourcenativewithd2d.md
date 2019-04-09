---
UID: NN:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D
title: ISurfaceImageSourceNativeWithD2D (windows.ui.xaml.media.dxinterop.h)
author: windows-sdk-content
description: Provides the implementation of a shared Microsoft DirectX surface which is displayed in a SurfaceImageSource or VirtualSurfaceImageSource.
old-location: winrt\isurfaceimagesourcenativewithd2d.htm
tech.root: WinRT
ms.assetid: 5C004E4F-12C6-4C2E-AE9A-D841411FF689
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNativeWithD2D, ISurfaceImageSourceNativeWithD2D interface [Windows Runtime], ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],described, windows/ISurfaceImageSourceNativeWithD2D, winrt.isurfaceimagesourcenativewithd2d
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
 - ISurfaceImageSourceNativeWithD2D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISurfaceImageSourceNativeWithD2D interface


## -description


Provides the implementation of a shared Microsoft DirectX surface which is displayed in a <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> or <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISurfaceImageSourceNativeWithD2D</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISurfaceImageSourceNativeWithD2D</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISurfaceImageSourceNativeWithD2D</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/077458AB-7644-4973-8955-95E097DAF859">BeginDraw</a>
</td>
<td align="left" width="63%">
Initiates an update to the associated <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> or <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E152D80-2673-43C6-B242-F89C890EE688">EndDraw</a>
</td>
<td align="left" width="63%">
Closes the surface draw operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A1FD29B-6340-49F5-BBF3-2E621FB16925">ResumeDraw</a>
</td>
<td align="left" width="63%">
Resume the drawing operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FBBF0A5E-68FF-4143-A874-0C1100100428">SetDevice</a>
</td>
<td align="left" width="63%">
Sets the DXGI or Direct2D device, created with <b>D3D11_CREATE_DEVICE_BGRA_SUPPORT</b>, that will draw the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/022B6A31-35B4-4E31-9B6E-12F75A156378">SuspendDraw</a>
</td>
<td align="left" width="63%">
Suspends the drawing operation.

</td>
</tr>
</table> 


## -remarks



The <b>ISurfaceImageSourceNativeWithD2D</b> interface provides the native implementation of the <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> class. To get a pointer to the  <b>ISurfaceImageSourceNativeWithD2D</b> interface, you must cast a <b>SurfaceImageSource</b> instance to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> or <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>, and call the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method.


```cpp

Microsoft::WRL::ComPtr<ISurfaceImageSourceNativeWithD2D>	m_sisD2DNative;
// ...
IInspectable* sisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(surfaceImageSource);
sisInspectable->QueryInterface(__uuidof(ISurfaceImageSourceNative), (void **)&m_sisD2DNative)
	
```


The <b>ISurfaceImageSourceNativeWithD2D</b> interface provides high-performance batched Direct2D drawing, which enables drawing to multiple different <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> or <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a> objects in the same batch, as long as they share the same Direct2D device.  Batching can improve performance when updating multiple surfaces at the same time.
 
 

The <b>ISurfaceImageSourceNativeWithD2D</b> interface enables drawing to a <a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a> or <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a> from one or more background threads, which allows high-performance DirectX rendering off the UI thread.

Only call the <a href="https://msdn.microsoft.com/FBBF0A5E-68FF-4143-A874-0C1100100428">SetDevice</a>, <a href="https://msdn.microsoft.com/077458AB-7644-4973-8955-95E097DAF859">BeginDraw</a>, and <a href="https://msdn.microsoft.com/1E152D80-2673-43C6-B242-F89C890EE688">EndDraw</a> methods on <b>ISurfaceImageSourceNativeWithD2D</b> interface, not on the <a href="https://msdn.microsoft.com/55122048-FA3B-494F-8BD3-97D2C36E4579">ISurfaceImageSourceNative</a> or <a href="https://msdn.microsoft.com/1CABA8F5-2380-45B9-804C-B1DC9FF34B62">IVirtualSurfaceImageSourceNative</a> interfaces.  



In order to support batching updates to multiple surfaces to improve performance, you can pass an <a href="https://msdn.microsoft.com/21f77c38-c115-4fdf-b294-570577a29201">ID2D1Device</a> to the <a href="https://msdn.microsoft.com/FBBF0A5E-68FF-4143-A874-0C1100100428">SetDevice</a> method, instead of an <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>.  The <a href="https://msdn.microsoft.com/077458AB-7644-4973-8955-95E097DAF859">BeginDraw</a> method can then optionally return a shared <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a>, which the app uses to draw all content for that update.

To draw to the surface from a background thread, you must set any DirectX resources, including the Microsoft Direct3D device, Direct3D device context, Direct2D device, and Direct2D device context, to enable multithreading support.  



You can call the <a href="https://msdn.microsoft.com/077458AB-7644-4973-8955-95E097DAF859">BeginDraw</a>, <a href="https://msdn.microsoft.com/022B6A31-35B4-4E31-9B6E-12F75A156378">SuspendDraw</a>, and <a href="https://msdn.microsoft.com/0A1FD29B-6340-49F5-BBF3-2E621FB16925">ResumeDraw</a> methods from any background thread to enable high-performance multithreaded drawing.

Always call the <a href="https://msdn.microsoft.com/1E152D80-2673-43C6-B242-F89C890EE688">EndDraw</a> method on the UI thread in order to synchronize updating the DirectX content with the current XAML UI thread frame.  You can call <a href="https://msdn.microsoft.com/077458AB-7644-4973-8955-95E097DAF859">BeginDraw</a> on a background thread, call <a href="https://msdn.microsoft.com/022B6A31-35B4-4E31-9B6E-12F75A156378">SuspendDraw</a> when you're done drawing on the background thread, and call <b>EndDraw</b> on the UI thread.

Use <a href="https://msdn.microsoft.com/022B6A31-35B4-4E31-9B6E-12F75A156378">SuspendDraw</a> and <a href="https://msdn.microsoft.com/0A1FD29B-6340-49F5-BBF3-2E621FB16925">ResumeDraw</a> to suspend and resume drawing on any background or UI thread.



Handle the <a href="https://msdn.microsoft.com/4ca7cb50-d2f5-484a-b700-1cda5bdb484a">SurfaceContentsLost</a> event to determine when you need to recreate content which may be lost if the system resets the GPU.




## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/4ca7cb50-d2f5-484a-b700-1cda5bdb484a">SurfaceContentsLost</a>



<a href="https://msdn.microsoft.com/fb58f405-895f-4590-8bff-7b1a9573791f">SurfaceImageSource</a>



<a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">VirtualSurfaceImageSource</a>
 

 

