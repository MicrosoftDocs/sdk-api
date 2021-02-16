---
UID: NF:dxgi1_2.IDXGIResource1.CreateSubresourceSurface
title: IDXGIResource1::CreateSubresourceSurface (dxgi1_2.h)
description: Creates a subresource surface object.
helpviewer_keywords: ["CreateSubresourceSurface","CreateSubresourceSurface method [DXGI]","CreateSubresourceSurface method [DXGI]","IDXGIResource1 interface","IDXGIResource1 interface [DXGI]","CreateSubresourceSurface method","IDXGIResource1.CreateSubresourceSurface","IDXGIResource1::CreateSubresourceSurface","direct3ddxgi.idxgiresource1_createsubresourcesurface","dxgi1_2/IDXGIResource1::CreateSubresourceSurface"]
old-location: direct3ddxgi\idxgiresource1_createsubresourcesurface.htm
tech.root: direct3ddxgi
ms.assetid: 99730AB1-C5D9-41D6-8001-495FF26E8232
ms.date: 12/05/2018
ms.keywords: CreateSubresourceSurface, CreateSubresourceSurface method [DXGI], CreateSubresourceSurface method [DXGI],IDXGIResource1 interface, IDXGIResource1 interface [DXGI],CreateSubresourceSurface method, IDXGIResource1.CreateSubresourceSurface, IDXGIResource1::CreateSubresourceSurface, direct3ddxgi.idxgiresource1_createsubresourcesurface, dxgi1_2/IDXGIResource1::CreateSubresourceSurface
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIResource1::CreateSubresourceSurface
 - dxgi1_2/IDXGIResource1::CreateSubresourceSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIResource1.CreateSubresourceSurface
---

# IDXGIResource1::CreateSubresourceSurface


## -description

Creates a subresource surface object.

## -parameters

### -param index

The index of the subresource surface object to enumerate.

### -param ppSurface [out]

The address of a pointer to a <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2">IDXGISurface2</a> interface that represents the created subresource surface object at the position specified by the <i>index</i> parameter.

## -returns

Returns S_OK if successful; otherwise, returns one of the following values:

<ul>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if the index is out of range or if the subresource is not a valid surface.</li>
<li>E_OUTOFMEMORY if insufficient memory is available to create the subresource surface object.</li>
</ul>
A subresource is a valid surface if the original resource would have been a valid surface had its array size been equal to 1.

## -remarks

Subresource surface objects implement the <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2">IDXGISurface2</a> interface, which inherits from  <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a> and indirectly <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>.  Therefore, the GDI-interoperable methods of <b>IDXGISurface1</b> work if the original resource interface object was created with the GDI-interoperable flag (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_GDI_COMPATIBLE</a>).

<b>CreateSubresourceSurface</b> creates a subresource surface that is based on the resource interface on which <b>CreateSubresourceSurface</b> is called. For example, if the original resource interface object is a 2D texture, the created subresource surface is also a 2D texture.

You can use <b>CreateSubresourceSurface</b> to create parts of  a stereo resource so you can use Direct2D on either the left or right part of the stereo resource.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1">IDXGIResource1</a>