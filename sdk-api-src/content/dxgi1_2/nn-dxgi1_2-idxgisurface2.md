---
UID: NN:dxgi1_2.IDXGISurface2
title: IDXGISurface2 (dxgi1_2.h)
description: The IDXGISurface2 interface extends the IDXGISurface1 interface by adding support for subresource surfaces and getting a handle to a shared resource.
helpviewer_keywords: ["IDXGISurface2","IDXGISurface2 interface [DXGI]","IDXGISurface2 interface [DXGI]","described","direct3ddxgi.idxgisurface2","dxgi1_2/IDXGISurface2"]
old-location: direct3ddxgi\idxgisurface2.htm
tech.root: direct3ddxgi
ms.assetid: EBBB2EE1-C5EA-4F98-AA8B-BCAA8C188F26
ms.date: 12/05/2018
ms.keywords: IDXGISurface2, IDXGISurface2 interface [DXGI], IDXGISurface2 interface [DXGI],described, direct3ddxgi.idxgisurface2, dxgi1_2/IDXGISurface2
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
 - IDXGISurface2
 - dxgi1_2/IDXGISurface2
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
 - IDXGISurface2
---

# IDXGISurface2 interface


## -description

The <b>IDXGISurface2</b> interface extends the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a> interface by adding support for subresource surfaces and getting a handle to a shared resource.

## -inheritance

The <b>IDXGISurface2</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a>. <b>IDXGISurface2</b> also has these types of members:

## -remarks

An image-data object is a 2D section of memory, commonly called a surface. To get the surface from an output, call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">IDXGIOutput::GetDisplaySurfaceData</a>. Then, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> object that <b>IDXGIOutput::GetDisplaySurfaceData</b> returns to retrieve the <b>IDXGISurface2</b> interface.

Any object that supports <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> also supports <b>IDXGISurface2</b>.

The runtime automatically creates an <b>IDXGISurface2</b> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface2</b> interface when you call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface2</b> interface that represents the 2D texture surface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">ID3D11Texture2D::QueryInterface</a>. In this call, you must pass the identifier of <b>IDXGISurface2</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface2</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface2</b>.

You can call the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface">IDXGIResource1::CreateSubresourceSurface</a> method to create an <b>IDXGISurface2</b> interface that refers to one subresource of a stereo resource.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface1">IDXGISurface1</a>
