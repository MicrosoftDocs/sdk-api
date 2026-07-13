---
UID: NF:d3d9.IDirect3D9Ex.GetAdapterLUID
title: IDirect3D9Ex::GetAdapterLUID (d3d9.h)
description: This method returns a unique identifier for the adapter that is specific to the adapter hardware. Applications can use this identifier to define robust mappings across various APIs (Direct3D 9, DXGI).
helpviewer_keywords: ["GetAdapterLUID","GetAdapterLUID method [Direct3D 9]","GetAdapterLUID method [Direct3D 9]","IDirect3D9Ex interface","IDirect3D9Ex interface [Direct3D 9]","GetAdapterLUID method","IDirect3D9Ex.GetAdapterLUID","IDirect3D9Ex::GetAdapterLUID","d3d9/IDirect3D9Ex::GetAdapterLUID","direct3d9.idirect3d9ex_getadapterluid","f330bb92-02a0-089a-4923-b68cf9e2282b"]
old-location: direct3d9\idirect3d9ex_getadapterluid.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_getadapterluid.htm
ms.date: 12/05/2018
ms.keywords: GetAdapterLUID, GetAdapterLUID method [Direct3D 9], GetAdapterLUID method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],GetAdapterLUID method, IDirect3D9Ex.GetAdapterLUID, IDirect3D9Ex::GetAdapterLUID, d3d9/IDirect3D9Ex::GetAdapterLUID, direct3d9.idirect3d9ex_getadapterluid, f330bb92-02a0-089a-4923-b68cf9e2282b
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3D9Ex::GetAdapterLUID
 - d3d9/IDirect3D9Ex::GetAdapterLUID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3D9Ex.GetAdapterLUID
---

# IDirect3D9Ex::GetAdapterLUID


## -description

This method returns a unique identifier for the adapter that is specific to the adapter hardware. Applications can use this identifier to define robust mappings across various APIs (Direct3D 9, DXGI).

## -parameters

### -param Adapter [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Ordinal number denoting the display adapter from which to retrieve the LUID.

### -param pLUID [in]

Type: <b><a href="/previous-versions/windows/hardware/drivers/ff549708(v=vs.85)">LUID</a>*</b>

A unique identifier for the given adapter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a>