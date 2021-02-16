---
UID: NF:dxgi1_4.IDXGIFactory4.EnumWarpAdapter
title: IDXGIFactory4::EnumWarpAdapter (dxgi1_4.h)
description: Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.
helpviewer_keywords: ["EnumWarpAdapter","EnumWarpAdapter method [DXGI]","EnumWarpAdapter method [DXGI]","IDXGIFactory4 interface","IDXGIFactory4 interface [DXGI]","EnumWarpAdapter method","IDXGIFactory4.EnumWarpAdapter","IDXGIFactory4::EnumWarpAdapter","direct3ddxgi.idxgifactory4_enumwarpadapter","dxgi1_4/IDXGIFactory4::EnumWarpAdapter"]
old-location: direct3ddxgi\idxgifactory4_enumwarpadapter.htm
tech.root: direct3ddxgi
ms.assetid: 18991B1A-5FA7-4298-A5FD-C8D7C485E4F7
ms.date: 12/05/2018
ms.keywords: EnumWarpAdapter, EnumWarpAdapter method [DXGI], EnumWarpAdapter method [DXGI],IDXGIFactory4 interface, IDXGIFactory4 interface [DXGI],EnumWarpAdapter method, IDXGIFactory4.EnumWarpAdapter, IDXGIFactory4::EnumWarpAdapter, direct3ddxgi.idxgifactory4_enumwarpadapter, dxgi1_4/IDXGIFactory4::EnumWarpAdapter
req.header: dxgi1_4.h
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory4::EnumWarpAdapter
 - dxgi1_4/IDXGIFactory4::EnumWarpAdapter
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
 - IDXGIFactory4.EnumWarpAdapter
---

# IDXGIFactory4::EnumWarpAdapter


## -description

Provides an adapter which can be provided to D3D12CreateDevice to use the WARP renderer.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) of the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> object referenced by the <i>ppvAdapter</i> parameter.

### -param ppvAdapter [out]

Type: <b>void**</b>

The address of an <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter">IDXGIAdapter</a> interface pointer to the adapter.
            This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; an error code otherwise.
            For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.
            See also Direct3D 12 Return Codes.

## -remarks

For more information, see <a href="/windows/desktop/direct3ddxgi/dxgi-1-4-improvements">DXGI 1.4 Improvements</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgifactory4">IDXGIFactory4</a>