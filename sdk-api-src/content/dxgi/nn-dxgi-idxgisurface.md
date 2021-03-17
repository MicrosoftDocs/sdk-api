---
UID: NN:dxgi.IDXGISurface
title: IDXGISurface (dxgi.h)
description: The IDXGISurface interface implements methods for image-data objects.
helpviewer_keywords: ["IDXGISurface","IDXGISurface interface [DXGI]","IDXGISurface interface [DXGI]","described","acd37adc-fb69-8924-76b4-598005b98bc9","direct3ddxgi.idxgisurface","dxgi/IDXGISurface"]
old-location: direct3ddxgi\idxgisurface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface.htm
ms.date: 12/05/2018
ms.keywords: IDXGISurface, IDXGISurface interface [DXGI], IDXGISurface interface [DXGI],described, acd37adc-fb69-8924-76b4-598005b98bc9, direct3ddxgi.idxgisurface, dxgi/IDXGISurface
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
 - IDXGISurface
 - dxgi/IDXGISurface
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
 - IDXGISurface
---

## -description

The  <b>IDXGISurface</b> interface implements methods for image-data objects.

## -inheritance

The <b>IDXGISurface</b> interface derives from <a href="/windows/win32/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>.

## -remarks

An image-data object is a 2D section of memory, commonly called a surface. To get the surface from an output, call <a href="/windows/win32/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">IDXGIOutput::GetDisplaySurfaceData</a>. 

Runtimes earlier than Direct3D 12 automatically create an <b>IDXGISurface</b> interface when they create a Direct3D resource object that represents a surface. <b>IDXGISurface</b> interfaces are not supported in Direct3D 12. For example, the runtime creates an <b>IDXGISurface</b> interface when you call <a href="/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> or <a href="/windows/win32/api/d3d10/nf-d3d10-id3d10device-createtexture2d">ID3D10Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface</b> interface that represents the 2D texture surface, call <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">ID3D11Texture2D::QueryInterface</a> or <b>ID3D10Texture2D::QueryInterface</b>. In this call, you must pass the identifier of <b>IDXGISurface</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface</b>.

## -see-also

<a href="/windows/win32/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>

<a href="/windows/win32/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>

