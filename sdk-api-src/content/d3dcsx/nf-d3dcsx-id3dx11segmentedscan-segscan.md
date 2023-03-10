---
UID: NF:d3dcsx.ID3DX11SegmentedScan.SegScan
title: ID3DX11SegmentedScan::SegScan (d3dcsx.h)
description: Performs a segmented scan of a sequence.
helpviewer_keywords: ["2c2b420b-cc9a-9f73-245d-047f419f53b4","ID3DX11SegmentedScan interface [Direct3D 11]","SegScan method","ID3DX11SegmentedScan.SegScan","ID3DX11SegmentedScan::SegScan","SegScan","SegScan method [Direct3D 11]","SegScan method [Direct3D 11]","ID3DX11SegmentedScan interface","d3dcsx/ID3DX11SegmentedScan::SegScan","direct3d11.id3dx11segmentedscan_segscan"]
old-location: direct3d11\id3dx11segmentedscan_segscan.htm
tech.root: direct3d11
ms.assetid: 096e1cc1-0bab-4e23-8c4c-47a2a0ff49fb
ms.date: 12/05/2018
ms.keywords: 2c2b420b-cc9a-9f73-245d-047f419f53b4, ID3DX11SegmentedScan interface [Direct3D 11],SegScan method, ID3DX11SegmentedScan.SegScan, ID3DX11SegmentedScan::SegScan, SegScan, SegScan method [Direct3D 11], SegScan method [Direct3D 11],ID3DX11SegmentedScan interface, d3dcsx/ID3DX11SegmentedScan::SegScan, direct3d11.id3dx11segmentedscan_segscan
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
 - ID3DX11SegmentedScan::SegScan
 - d3dcsx/ID3DX11SegmentedScan::SegScan
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
 - ID3DX11SegmentedScan.SegScan
---

# ID3DX11SegmentedScan::SegScan


## -description

Performs a segmented scan of a sequence.

## -parameters

### -param ElementType [in]

Type: <b><a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_data_type">D3DX11_SCAN_DATA_TYPE</a></b>

The type of element in the sequence.  See <a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_data_type">D3DX11_SCAN_DATA_TYPE</a> for more information.

### -param OpCode [in]

Type: <b><a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_opcode">D3DX11_SCAN_OPCODE</a></b>

The binary operation to perform.  See <a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_opcode">D3DX11_SCAN_OPCODE</a> for more information.

### -param ElementScanSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of scan in elements.

### -param pSrc [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Input sequence on the device.  Set <i>pSrc</i> and <i>pDst</i> to the same value for in-place scans.

### -param pSrcElementFlags [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Compact array of bits with one bit per element of <i>pSrc</i>.  A set value indicates the start of a new segment.

### -param pDst [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Output sequence on the device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

You must point the parameters <i>pSrc</i> and <i>pDst</i> to typed buffers (and not to raw or structured buffers). For information about buffer types, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-types">Types of Resources</a>. The format of these typed buffers must be <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R32_FLOAT</a>, <b>DXGI_FORMAT_R32_UINT</b>, or <b>DXGI_FORMAT_R32_INT</b>. In addition, the format of these typed buffers must match the scan data type that you specify in the <i>ElementType</i> parameter. For example, if the scan data type is <a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_scan_data_type">D3DX11_SCAN_DATA_TYPE_UINT</a>, the buffer formats must be <b>DXGI_FORMAT_R32_UINT</b>.

The format of the resource view to which the <i>pSrcElementFlags</i> parameter points must be <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_R32_UINT</a>.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11segmentedscan">ID3DX11SegmentedScan</a>