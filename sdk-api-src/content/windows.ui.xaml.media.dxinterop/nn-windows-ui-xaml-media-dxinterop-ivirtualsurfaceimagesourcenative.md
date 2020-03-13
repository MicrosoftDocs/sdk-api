---
UID: NN:windows.ui.xaml.media.dxinterop.IVirtualSurfaceImageSourceNative
title: IVirtualSurfaceImageSourceNative (windows.ui.xaml.media.dxinterop.h)
description: Provides the implementation of a large (greater than the screen size) shared surface for DirectX drawing.
old-location: winrt\ivirtualsurfaceimagesourcenative.htm
tech.root: WinRT
ms.assetid: 1CABA8F5-2380-45B9-804C-B1DC9FF34B62
ms.date: 12/05/2018
ms.keywords: IVirtualSurfaceImageSourceNative, IVirtualSurfaceImageSourceNative interface [Windows Runtime], IVirtualSurfaceImageSourceNative interface [Windows Runtime],described, windows/IVirtualSurfaceImageSourceNative, winrt.ivirtualsurfaceimagesourcenative
f1_keywords:
- windows.ui.xaml.media.dxinterop/IVirtualSurfaceImageSourceNative
dev_langs:
- c++
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
- IVirtualSurfaceImageSourceNative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVirtualSurfaceImageSourceNative interface


## -description


Provides the implementation of a large (greater than the screen size) shared surface for DirectX drawing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVirtualSurfaceImageSourceNative</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a>. <b>IVirtualSurfaceImageSourceNative</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-getupdaterectcount">GetUpdateRectCount</a>
</td>
<td align="left" width="63%">
Gets the total number of regions of the surface that must be updated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-getupdaterects">GetUpdateRects</a>
</td>
<td align="left" width="63%">
Gets the set of regions that must be updated on the shared surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-getvisiblebounds">GetVisibleBounds</a>
</td>
<td align="left" width="63%">
Gets the boundaries of the visible region of the shared surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-invalidate">Invalidate</a>
</td>
<td align="left" width="63%">
Invalidates a specific region of the shared surface for drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-registerforupdatesneeded">RegisterForUpdatesNeeded</a>
</td>
<td align="left" width="63%">
Registers for the callback that will perform the drawing when an update to the shared surface is requested.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative-resize">Resize</a>
</td>
<td align="left" width="63%">
Resizes the surface.

</td>
</tr>
</table> 


## -remarks



This interface provides the native implementation of the <a href="https://docs.microsoft.com/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">Windows::UI::Xaml::Media::Imaging::VirtualSurfaceImageSource</a> Windows runtime type. To obtain a pointer to <b>IVirtualSurfaceImageSourceNative</b>, you must cast a <b>VirtualSurfaceImageSource</b> instance to <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <b>IUnknown</b>, and call <b>QueryInterface</b>.


```cpp

Microsoft::WRL::ComPtr<IVirtualSurfaceImageSourceNative>	m_vsisNative;
// ...
IInspectable* vsisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(virtualSurfaceImageSource);
vsisInspectable->QueryInterface(__uuidof(IVirtualSurfaceImageSourceNative), (void **)&m_vsisNative)
	
```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a>
 

 

