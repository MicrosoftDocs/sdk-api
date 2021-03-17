---
UID: NF:d3dcsx.D3DX11CreateScan
title: D3DX11CreateScan function (d3dcsx.h)
description: Creates a scan context.
helpviewer_keywords: ["084772c2-3360-63d5-fb00-82f536323a9d","D3DX11CreateScan","D3DX11CreateScan function [Direct3D 11]","d3dcsx/D3DX11CreateScan","direct3d11.d3dx11createscan"]
old-location: direct3d11\d3dx11createscan.htm
tech.root: direct3d11
ms.assetid: daaa6913-a952-4f89-8a17-17e690ad8883
ms.date: 12/05/2018
ms.keywords: 084772c2-3360-63d5-fb00-82f536323a9d, D3DX11CreateScan, D3DX11CreateScan function [Direct3D 11], d3dcsx/D3DX11CreateScan, direct3d11.d3dx11createscan
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
 - D3DX11CreateScan
 - d3dcsx/D3DX11CreateScan
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
 - D3DX11CreateScan
---

# D3DX11CreateScan function


## -description

Creates a scan context.

## -parameters

### -param pDeviceContext [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>*</b>

The <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> the scan is associated with.

### -param MaxElementScanSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Maximum single scan size, in elements (FLOAT, UINT, or INT).

### -param MaxScanCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Maximum number of scans in multiscan.

### -param ppScan [out]

Type: <b><a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11scan">ID3DX11Scan</a>**</b>

Pointer to a <a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11scan">ID3DX11Scan Interface</a> pointer that will be set to the created interface object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The return value is one of the values listed in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-functions">D3DCSX 11 Functions</a>