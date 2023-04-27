---
UID: NF:d3dcsx.ID3DX11Scan.SetScanDirection
title: ID3DX11Scan::SetScanDirection (d3dcsx.h)
description: Sets which direction to perform scans in. (ID3DX11Scan.SetScanDirection)
helpviewer_keywords: ["ID3DX11Scan interface [Direct3D 11]","SetScanDirection method","ID3DX11Scan.SetScanDirection","ID3DX11Scan::SetScanDirection","SetScanDirection","SetScanDirection method [Direct3D 11]","SetScanDirection method [Direct3D 11]","ID3DX11Scan interface","d3dcsx/ID3DX11Scan::SetScanDirection","direct3d11.id3dx11scan_setscandirection","f86c1216-b196-31a2-2a44-3b56262de095"]
old-location: direct3d11\id3dx11scan_setscandirection.htm
tech.root: direct3d11
ms.assetid: f26b0e71-0803-4c57-b1bc-cefad5c449b7
ms.date: 12/05/2018
ms.keywords: ID3DX11Scan interface [Direct3D 11],SetScanDirection method, ID3DX11Scan.SetScanDirection, ID3DX11Scan::SetScanDirection, SetScanDirection, SetScanDirection method [Direct3D 11], SetScanDirection method [Direct3D 11],ID3DX11Scan interface, d3dcsx/ID3DX11Scan::SetScanDirection, direct3d11.id3dx11scan_setscandirection, f86c1216-b196-31a2-2a44-3b56262de095
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
 - ID3DX11Scan::SetScanDirection
 - d3dcsx/ID3DX11Scan::SetScanDirection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11Scan.SetScanDirection
---

# ID3DX11Scan::SetScanDirection


## -description

Sets which direction to perform scans in.

## -parameters

### -param Direction [in]

Type: <b><a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_direction">D3DX11_SCAN_DIRECTION</a></b>

Direction to perform scans in.  See <a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_direction">D3DX11_SCAN_DIRECTION</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<b>SetScanDirection</b> sets the direction <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11scan-scan">ID3DX11Scan::Scan</a> and <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11scan-multiscan">ID3DX11Scan::Multiscan</a> will performed scans in.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11scan">ID3DX11Scan</a>
