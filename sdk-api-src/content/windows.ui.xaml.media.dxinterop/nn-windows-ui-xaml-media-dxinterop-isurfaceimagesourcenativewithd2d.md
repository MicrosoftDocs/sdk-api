---
UID: NN:windows.ui.xaml.media.dxinterop.ISurfaceImageSourceNativeWithD2D
title: ISurfaceImageSourceNativeWithD2D (windows.ui.xaml.media.dxinterop.h)
description: Provides the implementation of a shared Microsoft DirectX surface which is displayed in a SurfaceImageSource or VirtualSurfaceImageSource.
helpviewer_keywords: ["ISurfaceImageSourceNativeWithD2D","ISurfaceImageSourceNativeWithD2D interface [Windows Runtime]","ISurfaceImageSourceNativeWithD2D interface [Windows Runtime]","described","windows/ISurfaceImageSourceNativeWithD2D","winrt.isurfaceimagesourcenativewithd2d"]
old-location: winrt\isurfaceimagesourcenativewithd2d.htm
tech.root: WinRT
ms.assetid: 5C004E4F-12C6-4C2E-AE9A-D841411FF689
ms.date: 12/05/2018
ms.keywords: ISurfaceImageSourceNativeWithD2D, ISurfaceImageSourceNativeWithD2D interface [Windows Runtime], ISurfaceImageSourceNativeWithD2D interface [Windows Runtime],described, windows/ISurfaceImageSourceNativeWithD2D, winrt.isurfaceimagesourcenativewithd2d
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISurfaceImageSourceNativeWithD2D
 - windows.ui.xaml.media.dxinterop/ISurfaceImageSourceNativeWithD2D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - ISurfaceImageSourceNativeWithD2D
---

# ISurfaceImageSourceNativeWithD2D interface


## -description

Provides the implementation of a shared Microsoft DirectX surface which is displayed in a <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> or <a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>.

## -inheritance

The <b>ISurfaceImageSourceNativeWithD2D</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISurfaceImageSourceNativeWithD2D</b> also has these types of members:

## -remarks

The <b>ISurfaceImageSourceNativeWithD2D</b> interface provides the native implementation of the <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> class. To get a pointer to the  <b>ISurfaceImageSourceNativeWithD2D</b> interface, you must cast a <b>SurfaceImageSource</b> instance to <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> or <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>, and call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method.


```cpp

Microsoft::WRL::ComPtr<ISurfaceImageSourceNativeWithD2D>	m_sisD2DNative;
// ...
IInspectable* sisInspectable = (IInspectable*) reinterpret_cast<IInspectable*>(surfaceImageSource);
sisInspectable->QueryInterface(__uuidof(ISurfaceImageSourceNative), (void **)&m_sisD2DNative)
	
```


The <b>ISurfaceImageSourceNativeWithD2D</b> interface provides high-performance batched Direct2D drawing, which enables drawing to multiple different <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> or <a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a> objects in the same batch, as long as they share the same Direct2D device.  Batching can improve performance when updating multiple surfaces at the same time.
 
 

The <b>ISurfaceImageSourceNativeWithD2D</b> interface enables drawing to a <a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a> or <a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a> from one or more background threads, which allows high-performance DirectX rendering off the UI thread.

Only call the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-setdevice">SetDevice</a>, <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-begindraw">BeginDraw</a>, and <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-enddraw">EndDraw</a> methods on <b>ISurfaceImageSourceNativeWithD2D</b> interface, not on the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative">ISurfaceImageSourceNative</a> or <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative">IVirtualSurfaceImageSourceNative</a> interfaces.  



In order to support batching updates to multiple surfaces to improve performance, you can pass an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a> to the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-setdevice">SetDevice</a> method, instead of an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>.  The <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-begindraw">BeginDraw</a> method can then optionally return a shared <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>, which the app uses to draw all content for that update.

To draw to the surface from a background thread, you must set any DirectX resources, including the Microsoft Direct3D device, Direct3D device context, Direct2D device, and Direct2D device context, to enable multithreading support.  



You can call the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-begindraw">BeginDraw</a>, <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-suspenddraw">SuspendDraw</a>, and <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-resumedraw">ResumeDraw</a> methods from any background thread to enable high-performance multithreaded drawing.

Always call the <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-enddraw">EndDraw</a> method on the UI thread in order to synchronize updating the DirectX content with the current XAML UI thread frame.  You can call <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-begindraw">BeginDraw</a> on a background thread, call <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-suspenddraw">SuspendDraw</a> when you're done drawing on the background thread, and call <b>EndDraw</b> on the UI thread.

Use <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-suspenddraw">SuspendDraw</a> and <a href="/windows/desktop/api/windows.ui.xaml.media.dxinterop/nf-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d-resumedraw">ResumeDraw</a> to suspend and resume drawing on any background or UI thread.



Handle the <a href="/uwp/api/windows.ui.xaml.media.compositiontarget.surfacecontentslost">SurfaceContentsLost</a> event to determine when you need to recreate content which may be lost if the system resets the GPU.

## -see-also

<a href="/previous-versions/windows/apps/hh825871(v=win.10)">DirectX and XAML interop</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/uwp/api/windows.ui.xaml.media.compositiontarget.surfacecontentslost">SurfaceContentsLost</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.surfaceimagesource">SurfaceImageSource</a>



<a href="/uwp/api/windows.ui.xaml.media.imaging.virtualsurfaceimagesource">VirtualSurfaceImageSource</a>
