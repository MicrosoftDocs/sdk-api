---
UID: NF:dxgi.IDXGISurface.GetDesc
title: IDXGISurface::GetDesc (dxgi.h)
description: Get a description of the surface.
helpviewer_keywords: ["92b3b49a-8f1d-7cd5-e484-3b5621c5acf5","GetDesc","GetDesc method [DXGI]","GetDesc method [DXGI]","IDXGISurface interface","IDXGISurface interface [DXGI]","GetDesc method","IDXGISurface.GetDesc","IDXGISurface::GetDesc","direct3ddxgi.idxgisurface_getdesc","dxgi/IDXGISurface::GetDesc"]
old-location: direct3ddxgi\idxgisurface_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_getdesc.htm
ms.date: 12/05/2018
ms.keywords: 92b3b49a-8f1d-7cd5-e484-3b5621c5acf5, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGISurface interface, IDXGISurface interface [DXGI],GetDesc method, IDXGISurface.GetDesc, IDXGISurface::GetDesc, direct3ddxgi.idxgisurface_getdesc, dxgi/IDXGISurface::GetDesc
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
 - IDXGISurface::GetDesc
 - dxgi/IDXGISurface::GetDesc
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
 - IDXGISurface.GetDesc
---

# IDXGISurface::GetDesc


## -description

Get a description of the surface.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_surface_desc">DXGI_SURFACE_DESC</a>*</b>

A pointer to the surface description (see <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_surface_desc">DXGI_SURFACE_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>