---
UID: NN:dxgi.IDXGISurface
title: IDXGISurface (dxgi.h)
author: windows-sdk-content
description: The IDXGISurface interface implements methods for image-data objects.
old-location: direct3ddxgi\idxgisurface.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGISurface, IDXGISurface interface [DXGI], IDXGISurface interface [DXGI],described, acd37adc-fb69-8924-76b4-598005b98bc9, direct3ddxgi.idxgisurface, dxgi/IDXGISurface
ms.topic: interface
f1_keywords: 
 - "dxgi/IDXGISurface"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISurface interface


## -description


The  <b>IDXGISurface</b> interface implements methods for image-data objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISurface</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>. <b>IDXGISurface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISurface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-map">Map</a>
</td>
<td align="left" width="63%">
Get a pointer to the data contained in the surface, and deny GPU access to the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-unmap">Unmap</a>
</td>
<td align="left" width="63%">
Invalidate the pointer to the surface retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-map">IDXGISurface::Map</a> and re-enable GPU access to the resource.

</td>
</tr>
</table> 


## -remarks



An image-data object is a 2D section of memory, commonly called a surface. To get the surface from an output, call <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-getdisplaysurfacedata">IDXGIOutput::GetDisplaySurfaceData</a>. 

The runtime automatically creates an <b>IDXGISurface</b> interface when it creates a Direct3D resource object that represents a surface. For example, the runtime creates an <b>IDXGISurface</b> interface when you call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture2d">ID3D10Device::CreateTexture2D</a> to create a 2D texture. To retrieve the <b>IDXGISurface</b> interface that represents the 2D texture surface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">ID3D11Texture2D::QueryInterface</a> or <b>ID3D10Texture2D::QueryInterface</b>. In this call, you must pass the identifier of <b>IDXGISurface</b>. If the 2D texture has only a single MIP-map level and does not consist of an array of textures, <b>QueryInterface</b> succeeds and returns a pointer to the <b>IDXGISurface</b> interface pointer. Otherwise, <b>QueryInterface</b> fails and does not return the pointer to <b>IDXGISurface</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>
 

 

