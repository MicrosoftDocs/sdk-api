---
UID: NF:dxgi.IDXGISurface.Unmap
title: IDXGISurface::Unmap (dxgi.h)
description: Invalidate the pointer to the surface retrieved by IDXGISurface::Map and re-enable GPU access to the resource.
helpviewer_keywords: ["72e0302e-2a02-c42b-8a5c-609c0e5f562a","IDXGISurface interface [DXGI]","Unmap method","IDXGISurface.Unmap","IDXGISurface::Unmap","Unmap","Unmap method [DXGI]","Unmap method [DXGI]","IDXGISurface interface","direct3ddxgi.idxgisurface_unmap","dxgi/IDXGISurface::Unmap"]
old-location: direct3ddxgi\idxgisurface_unmap.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_unmap.htm
ms.date: 12/05/2018
ms.keywords: 72e0302e-2a02-c42b-8a5c-609c0e5f562a, IDXGISurface interface [DXGI],Unmap method, IDXGISurface.Unmap, IDXGISurface::Unmap, Unmap, Unmap method [DXGI], Unmap method [DXGI],IDXGISurface interface, direct3ddxgi.idxgisurface_unmap, dxgi/IDXGISurface::Unmap
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
 - IDXGISurface::Unmap
 - dxgi/IDXGISurface::Unmap
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
 - IDXGISurface.Unmap
---

# IDXGISurface::Unmap


## -description

Invalidate the pointer to the surface retrieved by <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-map">IDXGISurface::Map</a> and re-enable GPU access to the resource.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>
