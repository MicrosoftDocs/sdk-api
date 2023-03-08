---
UID: NN:d2d1.ID2D1Factory
title: ID2D1Factory (d2d1.h)
description: Creates Direct2D resources. (ID2D1Factory)
helpviewer_keywords: ["ID2D1Factory","ID2D1Factory interface [Direct2D]","ID2D1Factory interface [Direct2D]","described","d2d1/ID2D1Factory","direct2d.ID2D1Factory"]
old-location: direct2d\ID2D1Factory.htm
tech.root: Direct2D
ms.assetid: cef6115c-98e8-49e6-b419-271b43ce2938
ms.date: 12/05/2018
ms.keywords: ID2D1Factory, ID2D1Factory interface [Direct2D], ID2D1Factory interface [Direct2D],described, d2d1/ID2D1Factory, direct2d.ID2D1Factory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory
 - d2d1/ID2D1Factory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory
---

# ID2D1Factory interface


## -description

Creates Direct2D resources.

## -inheritance

The <b>ID2D1Factory</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1Factory</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The <b>ID2D1Factory</b> interface is the starting point for using Direct2D; it's what you use to create other Direct2D resources that you can use to draw or describe shapes.   

A factory defines a set of Create<i>Resource</i> methods that can produce the following drawing resources:


<ul>
<li>Render targets: objects that render drawing commands.</li>
<li>Drawing state blocks: objects that store drawing state information, such as the current transformation and antialiasing mode.</li>
<li>Geometries: objects that represent simple and potentially complex shapes.</li>
</ul>


To create an <b>ID2D1Factory</b>, you use one of the <a href="/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory">CreateFactory</a> methods. You should retain the <b>ID2D1Factory</b> instance for as long as you use Direct2D resources; in general, you shouldn't need to recreate it when the application is running. For more information about Direct2D resources, see the <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.

<h3><a id="Singlethreaded_and_Multithreaded_Factories"></a><a id="singlethreaded_and_multithreaded_factories"></a><a id="SINGLETHREADED_AND_MULTITHREADED_FACTORIES"></a>Singlethreaded and Multithreaded Factories</h3>
When you create a factory, you can specify whether it is multithreaded or singlethreaded. A singlethreaded factory provides no serialization against any other single threaded instance within Direct2D, so, this mechanism provides a very large degree of scaling on the CPU.

You can also create a multithreaded factory instance. In this case, the factory and all derived objects can be used from any thread and each render target can be rendered to independently. Direct2D serializes calls to these objects, so a single multithreaded Direct2D instance won't scale as well on the CPU as many single threaded instances. However, the resources can be shared within the multithreaded instance.

Note that the qualifier "On the CPU": GPUs generally take advantage of fine-grained parallelism more so than CPUs. For example, multithreaded calls from the CPU might still end up being serialized when being sent to the GPU, however, a whole bank of pixel and vertex shaders will run in parallel to perform the rendering.



See <a href="/windows/win32/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a> for more info.


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

<a href="/windows/win32/Direct2D/direct2d-overview">Direct2D Overview</a>



[Create a simple Direct2D application](/windows/win32/Direct2D/direct2d-quickstart)



<a href="/windows/win32/Direct2D/getting-started-with-direct2d">Getting Started with Direct2D</a>



<a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/win32/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a>



<a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>

