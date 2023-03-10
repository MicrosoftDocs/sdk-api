---
UID: NF:d3dcsx.D3DX11CreateSegmentedScan
title: D3DX11CreateSegmentedScan function (d3dcsx.h)
description: Creates a segmented scan context.
helpviewer_keywords: ["6b834305-1925-9f3d-ee71-8dc858a331c0","D3DX11CreateSegmentedScan","D3DX11CreateSegmentedScan function [Direct3D 11]","d3dcsx/D3DX11CreateSegmentedScan","direct3d11.d3dx11createsegmentedscan"]
old-location: direct3d11\d3dx11createsegmentedscan.htm
tech.root: direct3d11
ms.assetid: f8906357-57d8-4e57-a120-2ac28fad2288
ms.date: 12/05/2018
ms.keywords: 6b834305-1925-9f3d-ee71-8dc858a331c0, D3DX11CreateSegmentedScan, D3DX11CreateSegmentedScan function [Direct3D 11], d3dcsx/D3DX11CreateSegmentedScan, direct3d11.d3dx11createsegmentedscan
req.header: d3dcsx.h
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
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DX11CreateSegmentedScan
 - d3dcsx/D3DX11CreateSegmentedScan
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - D3DX11CreateSegmentedScan
---

# D3DX11CreateSegmentedScan function


## -description

Creates a segmented scan context.

## -parameters

### -param pDeviceContext [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface.

### -param MaxElementScanSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Maximum single scan size, in elements (FLOAT, UINT, or INT).

### -param ppScan [out]

Type: <b><a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11segmentedscan">ID3DX11SegmentedScan</a>**</b>

Pointer to a <a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11segmentedscan">ID3DX11SegmentedScan Interface</a> pointer that will be set to the created interface object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The return value is one of the values listed in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-functions">D3DCSX 11 Functions</a>