---
UID: NN:d2d1.ID2D1Factory
title: ID2D1Factory (d2d1.h)
description: Creates Direct2D resources.helpviewer_keywords: ["ID2D1Factory","ID2D1Factory interface [Direct2D]","ID2D1Factory interface [Direct2D]","described","d2d1/ID2D1Factory","direct2d.ID2D1Factory"]
old-location: direct2d\ID2D1Factory.htm
tech.root: Direct2D
ms.assetid: cef6115c-98e8-49e6-b419-271b43ce2938
ms.date: 12/05/2018
ms.keywords: ID2D1Factory, ID2D1Factory interface [Direct2D], ID2D1Factory interface [Direct2D],described, d2d1/ID2D1Factory, direct2d.ID2D1Factory
f1_keywords:
- d2d1/ID2D1Factory
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory interface


## -description


Creates Direct2D resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Factory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1Factory</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget">CreateDCRenderTarget</a>
</td>
<td align="left" width="63%">
Creates a render target that draws to a Windows Graphics Device Interface (GDI) device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1factory-createdrawingstateblock">CreateDrawingStateBlock</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a> that can be used with the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-savedrawingstate">SaveDrawingState</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-restoredrawingstate">RestoreDrawingState</a> methods of a render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-createdxgisurfacerendertarget">CreateDxgiSurfaceRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-createellipsegeometry">CreateEllipseGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1ellipsegeometry">ID2D1EllipseGeometry</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup">CreateGeometryGroup</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1geometrygroup">ID2D1GeometryGroup</a>, which is an object that holds other geometries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-createhwndrendertarget">CreateHwndRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a>, a render target that renders to a window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry">CreatePathGeometry</a>
</td>
<td align="left" width="63%">
Creates an empty <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1pathgeometry">ID2D1PathGeometry</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-createrectanglegeometry">CreateRectangleGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rectanglegeometry">ID2D1RectangleGeometry</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-createroundedrectanglegeometry">CreateRoundedRectangleGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry">ID2D1RoundedRectangleGeometry</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1factory-createstrokestyle">CreateStrokeStyle</a>
</td>
<td align="left" width="63%">Overloaded. Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1strokestyle">ID2D1StrokeStyle</a> that describes start cap, dash pattern, and other features of a stroke.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-createtransformedgeometry">CreateTransformedGeometry</a>
</td>
<td align="left" width="63%">Overloaded. Transforms the specified geometry and stores the result as an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1transformedgeometry">ID2D1TransformedGeometry</a> object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/Direct2D/id2d1factory-createwicbitmaprendertarget">CreateWicBitmapRenderTarget</a>
</td>
<td align="left" width="63%">Overloaded. Creates a render target that renders to a Microsoft Windows Imaging Component (WIC)  bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi">GetDesktopDpi</a>
</td>
<td align="left" width="63%">
Retrieves the current desktop dots per inch (DPI). To refresh this value, call <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-reloadsystemmetrics">ReloadSystemMetrics</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-reloadsystemmetrics">ReloadSystemMetrics</a>
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


To create an <b>ID2D1Factory</b>, you use one of the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory">CreateFactory</a> methods. You should retain the <b>ID2D1Factory</b> instance for as long as you use Direct2D resources; in general, you shouldn't need to recreate it when the application is running. For more information about Direct2D resources, see the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>.

<h3><a id="Singlethreaded_and_Multithreaded_Factories"></a><a id="singlethreaded_and_multithreaded_factories"></a><a id="SINGLETHREADED_AND_MULTITHREADED_FACTORIES"></a>Singlethreaded and Multithreaded Factories</h3>
When you create a factory, you can specify whether it is multithreaded or singlethreaded. A singlethreaded factory provides no serialization against any other single threaded instance within Direct2D, so, this mechanism provides a very large degree of scaling on the CPU.

You can also create a multithreaded factory instance. In this case, the factory and all derived objects can be used from any thread and each render target can be rendered to independently. Direct2D serializes calls to these objects, so a single multithreaded Direct2D instance won't scale as well on the CPU as many single threaded instances. However, the resources can be shared within the multithreaded instance.

Note that the qualifier "On the CPU": GPUs generally take advantage of fine-grained parallelism more so than CPUs. For example, multithreaded calls from the CPU might still end up being serialized when being sent to the GPU, however, a whole bank of pixel and vertex shaders will run in parallel to perform the rendering.



See <a href="https://docs.microsoft.com/windows/desktop/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a> for more info.


## Examples

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




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-overview">Direct2D Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-quickstart">Direct2D QuickStart</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/getting-started-with-direct2d">Getting Started with Direct2D</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a>



<a href="https://docs.microsoft.com/windows/desktop/Direct2D/resources-and-resource-domains">Resources Overview</a>
 

 

