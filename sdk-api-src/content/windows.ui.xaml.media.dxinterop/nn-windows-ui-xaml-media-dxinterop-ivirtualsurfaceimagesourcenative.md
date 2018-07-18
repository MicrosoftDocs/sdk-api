---
UID: NN:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative
title: IVirtualSurfaceImageSourceNative
author: windows-sdk-content
description: Provides the implementation of a large (greater than the screen size) shared surface for DirectX drawing.
old-location: winrt\ivirtualsurfaceimagesourcenative.htm
old-project: WinRT
ms.assetid: 1CABA8F5-2380-45B9-804C-B1DC9FF34B62
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IVirtualSurfaceImageSourceNative, IVirtualSurfaceImageSourceNative interface [Windows Runtime], IVirtualSurfaceImageSourceNative interface [Windows Runtime],described, windows/IVirtualSurfaceImageSourceNative, winrt.ivirtualsurfaceimagesourcenative
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
 - IVirtualSurfaceImageSourceNative
product: Windows
targetos: Windows
req.lib: 
req.dll: Windows.UI.Xaml.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IVirtualSurfaceImageSourceNative interface


## -description


Provides the implementation of a large (greater than the screen size) shared surface for DirectX drawing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVirtualSurfaceImageSourceNative</b> interface inherits from <a href="https://msdn.microsoft.com/55122048-FA3B-494F-8BD3-97D2C36E4579">ISurfaceImageSourceNative</a>. <b>IVirtualSurfaceImageSourceNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVirtualSurfaceImageSourceNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE717587-0156-4DEC-B7B2-FF8937117D5A">GetUpdateRectCount</a>
</td>
<td align="left" width="63%">
Gets the total number of regions of the surface that must be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C23F3F82-FB3B-4893-8C14-FC7D3C61D295">GetUpdateRects</a>
</td>
<td align="left" width="63%">
Gets the set of regions that must be updated on the shared surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C296DD29-97C8-4C4E-A424-33DDC37538A9">GetVisibleBounds</a>
</td>
<td align="left" width="63%">
Gets the boundaries of the visible region of the shared surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BC3BC983-9A78-4B0F-927D-06B299031C80">Invalidate</a>
</td>
<td align="left" width="63%">
Invalidates a specific region of the shared surface for drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D12AE5FD-ED3D-49E5-8E41-B1598C64A108">RegisterForUpdatesNeeded</a>
</td>
<td align="left" width="63%">
Registers for the callback that will perform the drawing when an update to the shared surface is requested.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09808606-9735-4838-BE32-F10B172FD7A9">Resize</a>
</td>
<td align="left" width="63%">
Resizes the surface.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://msdn.microsoft.com/7a28cfdd-44d4-4aa7-b57e-a5fbdf66bee3">Windows::UI::Xaml::Media::Imaging::VirtualSurfaceImageSource</a> Windows runtime type. To obtain a pointer to <b>IVirtualSurfaceImageSourceNative</b>, you must cast a <b>VirtualSurfaceImageSource</b> instance to <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
Microsoft::WRL::ComPtr&lt;IVirtualSurfaceImageSourceNative&gt;	m_vsisNative;
// ...
IInspectable* vsisInspectable = (IInspectable*) reinterpret_cast&lt;IInspectable*&gt;(virtualSurfaceImageSource);
vsisInspectable-&gt;QueryInterface(__uuidof(IVirtualSurfaceImageSourceNative), (void **)&amp;m_vsisNative)
	</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/17987EEA-6771-423C-9B68-6B9AEADC7B7F">DirectX and XAML interop</a>



<a href="https://msdn.microsoft.com/55122048-FA3B-494F-8BD3-97D2C36E4579">ISurfaceImageSourceNative</a>
 

 

