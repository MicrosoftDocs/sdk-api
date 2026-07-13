---
UID: NN:dxgi.IDXGIObject
title: IDXGIObject (dxgi.h)
description: An IDXGIObject interface is a base interface for all DXGI objects; IDXGIObject supports associating caller-defined (private data) with an object and retrieval of an interface to the parent object.
helpviewer_keywords: ["IDXGIObject","IDXGIObject interface [DXGI]","IDXGIObject interface [DXGI]","described","ae721ac9-3ed3-d7ef-07a7-3f3acbb19dcd","direct3ddxgi.idxgiobject","dxgi/IDXGIObject"]
old-location: direct3ddxgi\idxgiobject.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiobject.htm
ms.date: 12/05/2018
ms.keywords: IDXGIObject, IDXGIObject interface [DXGI], IDXGIObject interface [DXGI],described, ae721ac9-3ed3-d7ef-07a7-3f3acbb19dcd, direct3ddxgi.idxgiobject, dxgi/IDXGIObject
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIObject
 - dxgi/IDXGIObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIObject
---

# IDXGIObject interface


## -description

An <b>IDXGIObject</b> interface is a base interface for all DXGI objects;
        <b>IDXGIObject</b> supports associating caller-defined (private data) with an object and retrieval of an interface to the parent object.

## -inheritance

The <b>IDXGIObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIObject</b> also has these types of members:

## -remarks

<b>IDXGIObject</b> implements base-class functionality for the following interfaces:
        

<ul>
<li>
<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a>
</li>
<li>
<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>
</li>
<li>
<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>
</li>
<li>
<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>
</li>
</ul>
<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
