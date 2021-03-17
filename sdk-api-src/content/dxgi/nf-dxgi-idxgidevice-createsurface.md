---
UID: NF:dxgi.IDXGIDevice.CreateSurface
title: IDXGIDevice::CreateSurface (dxgi.h)
description: Returns a surface. This method is used internally and you should not call it directly in your application.
helpviewer_keywords: ["CreateSurface","CreateSurface method [DXGI]","CreateSurface method [DXGI]","IDXGIDevice interface","IDXGIDevice interface [DXGI]","CreateSurface method","IDXGIDevice.CreateSurface","IDXGIDevice::CreateSurface","a6514b10-4398-2f19-86d3-e31bb2c9044c","direct3ddxgi.idxgidevice_createsurface","dxgi/IDXGIDevice::CreateSurface"]
old-location: direct3ddxgi\idxgidevice_createsurface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgidevice_createsurface.htm
ms.date: 12/05/2018
ms.keywords: CreateSurface, CreateSurface method [DXGI], CreateSurface method [DXGI],IDXGIDevice interface, IDXGIDevice interface [DXGI],CreateSurface method, IDXGIDevice.CreateSurface, IDXGIDevice::CreateSurface, a6514b10-4398-2f19-86d3-e31bb2c9044c, direct3ddxgi.idxgidevice_createsurface, dxgi/IDXGIDevice::CreateSurface
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
 - IDXGIDevice::CreateSurface
 - dxgi/IDXGIDevice::CreateSurface
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
 - IDXGIDevice.CreateSurface
---

# IDXGIDevice::CreateSurface


## -description

Returns a surface. This method is used internally and you should not call it directly in your application.

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_surface_desc">DXGI_SURFACE_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_surface_desc">DXGI_SURFACE_DESC</a> structure that describes the surface.

### -param NumSurfaces

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of surfaces to create.

### -param Usage

Type: <b><a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE</a></b>

A <a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE</a> flag that specifies how the surface is expected to be used.

### -param pSharedResource [in, optional]

Type: <b>const <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_shared_resource">DXGI_SHARED_RESOURCE</a>*</b>

An optional pointer to a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_shared_resource">DXGI_SHARED_RESOURCE</a> structure that contains shared resource information for opening views of such resources.

### -param ppSurface [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>**</b>

The address of an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> interface pointer to the first created surface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

The <b>CreateSurface</b> method creates a buffer to exchange data between one or more devices. It is used internally, and you should not directly call it.

The runtime automatically creates an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface</b> interface when it calls <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> or <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture2d">ID3D10Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface</b> interface that represents the 2D texture surface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">ID3D11Texture2D::QueryInterface</a> or <b>ID3D10Texture2D::QueryInterface</b>. In this call, you must pass the identifier of <b>IDXGISurface</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface</b>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture2d">ID3D10Device::CreateTexture2D</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevice">IDXGIDevice</a>