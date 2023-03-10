---
UID: NE:d2d1.D2D1_FACTORY_TYPE
title: D2D1_FACTORY_TYPE (d2d1.h)
description: Specifies whether Direct2D provides synchronization for an ID2D1Factory and the resources it creates, so that they may be safely accessed from multiple threads.
helpviewer_keywords: ["D2D1_FACTORY_TYPE","D2D1_FACTORY_TYPE enumeration [Direct2D]","D2D1_FACTORY_TYPE_MULTI_THREADED","D2D1_FACTORY_TYPE_SINGLE_THREADED","d2d1/D2D1_FACTORY_TYPE","d2d1/D2D1_FACTORY_TYPE_MULTI_THREADED","d2d1/D2D1_FACTORY_TYPE_SINGLE_THREADED","direct2d.D2D1_FACTORY_TYPE"]
old-location: direct2d\D2D1_FACTORY_TYPE.htm
tech.root: Direct2D
ms.assetid: 428053d3-7ea0-4b01-9924-4a31d8e018fb
ms.date: 12/05/2018
ms.keywords: D2D1_FACTORY_TYPE, D2D1_FACTORY_TYPE enumeration [Direct2D], D2D1_FACTORY_TYPE_MULTI_THREADED, D2D1_FACTORY_TYPE_SINGLE_THREADED, d2d1/D2D1_FACTORY_TYPE, d2d1/D2D1_FACTORY_TYPE_MULTI_THREADED, d2d1/D2D1_FACTORY_TYPE_SINGLE_THREADED, direct2d.D2D1_FACTORY_TYPE
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_FACTORY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FACTORY_TYPE
 - d2d1/D2D1_FACTORY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_FACTORY_TYPE
---

# D2D1_FACTORY_TYPE enumeration


## -description

Specifies whether Direct2D provides synchronization for an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a> and the resources it creates, so that they may be safely accessed from multiple threads.

## -enum-fields

### -field D2D1_FACTORY_TYPE_SINGLE_THREADED:0

No synchronization is provided for accessing or writing to the factory or the objects it creates. If the factory or the objects are called from multiple threads, it is up to the application to provide access locking.

### -field D2D1_FACTORY_TYPE_MULTI_THREADED:1

Direct2D provides synchronization for accessing and writing to the factory and the objects it creates, enabling safe access from multiple threads.

### -field D2D1_FACTORY_TYPE_FORCE_DWORD:0xffffffff

## -remarks

When you create a factory, you can specify whether it is multithreaded or singlethreaded. A singlethreaded factory provides no serialization against any other single threaded instance within Direct2D, so this mechanism provides a very large degree of scaling on the CPU.

You can also create a multithreaded factory instance. In this case, the factory and all derived objects can be used from any thread, and each render target can be rendered to independently. Direct2D serializes calls to these objects, so a single multithreaded Direct2D instance won't scale as well on the CPU as many single threaded instances. However, the resources can be shared within the multithreaded instance.

Note the qualifier "On the CPU": GPUs generally take advantage of fine-grained parallelism more so than CPUs. For example, multithreaded calls from the CPU might still end up being serialized when being sent to the GPU; however, a whole bank of pixel and vertex shaders will run in parallel to perform the rendering.


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

<a href="/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory">CreateFactory</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>



<a href="/windows/win32/Direct2D/multi-threaded-direct2d-apps">Multithreaded Direct2D Apps</a>

