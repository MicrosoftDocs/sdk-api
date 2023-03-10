---
UID: NF:dxgi.IDXGISurface.Map
title: IDXGISurface::Map (dxgi.h)
description: Get a pointer to the data contained in the surface, and deny GPU access to the surface.
helpviewer_keywords: ["2353661a-8e73-6878-2899-79d0afdc2901","IDXGISurface interface [DXGI]","Map method","IDXGISurface.Map","IDXGISurface::Map","Map","Map method [DXGI]","Map method [DXGI]","IDXGISurface interface","direct3ddxgi.idxgisurface_map","dxgi/IDXGISurface::Map"]
old-location: direct3ddxgi\idxgisurface_map.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgisurface_map.htm
ms.date: 12/05/2018
ms.keywords: 2353661a-8e73-6878-2899-79d0afdc2901, IDXGISurface interface [DXGI],Map method, IDXGISurface.Map, IDXGISurface::Map, Map, Map method [DXGI], Map method [DXGI],IDXGISurface interface, direct3ddxgi.idxgisurface_map, dxgi/IDXGISurface::Map
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
 - IDXGISurface::Map
 - dxgi/IDXGISurface::Map
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
 - IDXGISurface.Map
---

# IDXGISurface::Map


## -description

Get a pointer to the data contained in the surface, and deny GPU access to the surface.

## -parameters

### -param pLockedRect [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_mapped_rect">DXGI_MAPPED_RECT</a>*</b>

A pointer to the surface data (see <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_mapped_rect">DXGI_MAPPED_RECT</a>).

### -param MapFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

CPU read-write flags. These flags can be combined with a logical OR.



<ul>
<li>DXGI_MAP_READ - Allow CPU read access.</li>
<li>DXGI_MAP_WRITE - Allow CPU write access.</li>
<li>DXGI_MAP_DISCARD - Discard the previous contents of a resource when it is mapped.</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -remarks

Use <b>IDXGISurface::Map</b> to access a surface from the CPU. To release a mapped surface (and allow GPU access) call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgisurface-unmap">IDXGISurface::Unmap</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>