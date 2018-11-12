---
UID: NN:d2d1.ID2D1Factory
title: ID2D1Factory
author: windows-sdk-content
description: Creates Direct2D resources.
old-location: direct2d\ID2D1Factory.htm
tech.root: direct2d
ms.assetid: cef6115c-98e8-49e6-b419-271b43ce2938
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ID2D1Factory, ID2D1Factory interface [Direct2D], ID2D1Factory interface [Direct2D],described, d2d1/ID2D1Factory, direct2d.ID2D1Factory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory interface


## -description


Creates Direct2D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Factory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID2D1Factory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Factory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de062068-d2b5-4576-a475-a0e2c9840506">CreateDCRenderTarget</a>
</td>
<td align="left" width="63%">
Creates a render target that draws to a Windows Graphics Device Interface (GDI) device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2b5875f-9f14-4752-a426-2745fdaa543a">CreateDrawingStateBlock</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a> that can be used with the <a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a> and <a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a> methods of a render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/101744ea-97bc-4f92-88b0-fcdf0e4aaf4e">CreateDxgiSurfaceRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c03bb0b-74fe-456a-aa26-5449d758c0ea">CreateEllipseGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/4ab6452c-6df8-46c0-9e0d-0cebc19d84ba">ID2D1EllipseGeometry</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e69c54b9-eb10-4a7f-8a5b-c42ad4572fa0">CreateGeometryGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/15c3800c-b57c-4c3c-995f-407beee4cc99">ID2D1GeometryGroup</a>, which is an object that holds other geometries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b55b1b0-a423-40dc-9581-c1fbe8134ca5">CreateHwndRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35c46055-3df2-44d5-b11d-520ab2fa4a0e">CreatePathGeometry</a>
</td>
<td align="left" width="63%">
Creates an empty <a href="https://msdn.microsoft.com/d200563c-d78e-4fa0-a8f2-242b24480e99">ID2D1PathGeometry</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c8f4950-7b5a-4f77-9a5b-513916f83d0c">CreateRectangleGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/bb5f65ba-34d4-418b-863c-2431046bce8e">ID2D1RectangleGeometry</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f7ccb0-5733-4f96-a532-8f665fbc257e">CreateRoundedRectangleGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/e49e9be7-155a-4487-9931-035f18771c04">ID2D1RoundedRectangleGeometry</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc7bd68b-a6eb-4d05-b331-032ce80f375c">CreateStrokeStyle</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://msdn.microsoft.com/2cdf66dc-f34f-4132-8c06-7464648d3cef">ID2D1StrokeStyle</a> that describes start cap, dash pattern, and other features of a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71f26200-0f35-49d7-951d-2962768d16bc">CreateTransformedGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Transforms the specified geometry and stores the result as an <a href="https://msdn.microsoft.com/5d48eab6-1229-4e54-bfab-602b471b23a4">ID2D1TransformedGeometry</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93141743-c11d-40b4-83c5-07c9066836c7">CreateWicBitmapRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates a render target that renders to a Microsoft Windows Imaging Component (WIC)  bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd46252b-80eb-42c2-a2b4-5c49ef124bd5">GetDesktopDpi</a>
</td>
<td align="left" width="63%">
Retrieves the current desktop dots per inch (DPI). To refresh this value, call <a href="https://msdn.microsoft.com/32c831c4-73e1-49f8-8d58-4248ae99fe37">ReloadSystemMetrics</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32c831c4-73e1-49f8-8d58-4248ae99fe37">ReloadSystemMetrics</a>
</td>
<td align="left" width="63%">
Forces the factory to refresh any system defaults that it might have changed since factory creation.

</td>
</tr>
</table> 


## -remarks



The <b>ID2D1Factory</b> interface is the starting point for using Direct2D; it's what you use to create other Direct2D resources that you can use to draw or describe shapes.   

A factory defines a set of Create<i>Resource</i> methods that can produce the following drawing resources:


<ul>
<li>Render targets: objects that render drawing commands.</li>
<li>Drawing state blocks: objects that store drawing state information, such as the current transformation and antialiasing mode.</li>
<li>Geometries: objects that represent simple and potentially complex shapes.</li>
</ul>


To create an <b>ID2D1Factory</b>, you use one of the <a href="https://msdn.microsoft.com/8c0a685a-8f33-4072-a715-bb423cb44f03">CreateFactory</a> methods. You should retain the <b>ID2D1Factory</b> instance for as long as you use Direct2D resources; in general, you shouldn't need to recreate it when the application is running. For more information about Direct2D resources, see the <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.

<h3><a id="Singlethreaded_and_Multithreaded_Factories"></a><a id="singlethreaded_and_multithreaded_factories"></a><a id="SINGLETHREADED_AND_MULTITHREADED_FACTORIES"></a>Singlethreaded and Multithreaded Factories</h3>
When you create a factory, you can specify whether it is multithreaded or singlethreaded. A singlethreaded factory provides no serialization against any other single threaded instance within Direct2D, so, this mechanism provides a very large degree of scaling on the CPU.

You can also create a multithreaded factory instance. In this case, the factory and all derived objects can be used from any thread and each render target can be rendered to independently. Direct2D serializes calls to these objects, so a single multithreaded Direct2D instance won't scale as well on the CPU as many single threaded instances. However, the resources can be shared within the multithreaded instance.

Note that the qualifier "On the CPU": GPUs generally take advantage of fine-grained parallelism more so than CPUs. For example, multithreaded calls from the CPU might still end up being serialized when being sent to the GPU, however, a whole bank of pixel and vertex shaders will run in parallel to perform the rendering.



See <a href="https://msdn.microsoft.com/FDD770D4-817F-44D9-86C4-15DD04D214AE">Multithreaded Direct2D Apps</a> for more info.


#### Examples

The following code fragments declare a factory pointer, create a singlethreaded factory instance, and use the factory to create a render target.


```cpp
ID2D1Factory* m_pDirect2dFactory;

```

```cpp
    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

```

```cpp
        // Create a Direct2D render target.
        hr = m_pDirect2dFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );

```





## -see-also




<a href="https://msdn.microsoft.com/05cc230e-6fec-4a15-8e28-c68397392fc5">Direct2D Overview</a>



<a href="https://msdn.microsoft.com/a627523e-417a-40cd-82c0-4f0380a3a0b1">Direct2D QuickStart</a>



<a href="https://msdn.microsoft.com/19d9ad76-b1e3-449f-8582-e00287b05874">Getting Started with Direct2D</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/FDD770D4-817F-44D9-86C4-15DD04D214AE">Multithreaded Direct2D Apps</a>



<a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>
 

 

