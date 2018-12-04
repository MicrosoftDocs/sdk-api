---
UID: NF:d3dcsx.ID3DX11SegmentedScan.SegScan
title: ID3DX11SegmentedScan::SegScan
author: windows-sdk-content
description: Performs a segmented scan of a sequence.
old-location: direct3d11\id3dx11segmentedscan_segscan.htm
tech.root: direct3d11
ms.assetid: 096e1cc1-0bab-4e23-8c4c-47a2a0ff49fb
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: 2c2b420b-cc9a-9f73-245d-047f419f53b4, ID3DX11SegmentedScan interface [Direct3D 11],SegScan method, ID3DX11SegmentedScan.SegScan, ID3DX11SegmentedScan::SegScan, SegScan, SegScan method [Direct3D 11], SegScan method [Direct3D 11],ID3DX11SegmentedScan interface, d3dcsx/ID3DX11SegmentedScan::SegScan, direct3d11.id3dx11segmentedscan_segscan
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3DX11SegmentedScan::SegScan


## -description


Performs a segmented scan of a sequence.


## -parameters




### -param ElementType [in]

Type: <b><a href="https://msdn.microsoft.com/28bef01c-2d04-48f8-994b-86194f530610">D3DX11_SCAN_DATA_TYPE</a></b>

The type of element in the sequence.  See <a href="https://msdn.microsoft.com/28bef01c-2d04-48f8-994b-86194f530610">D3DX11_SCAN_DATA_TYPE</a> for more information.


### -param OpCode [in]

Type: <b><a href="https://msdn.microsoft.com/eba6912b-0e24-4c61-9c8e-fe801bf709e2">D3DX11_SCAN_OPCODE</a></b>

The binary operation to perform.  See <a href="https://msdn.microsoft.com/eba6912b-0e24-4c61-9c8e-fe801bf709e2">D3DX11_SCAN_OPCODE</a> for more information.


### -param ElementScanSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Size of scan in elements.


### -param pSrc [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Input sequence on the device.  Set <i>pSrc</i> and <i>pDst</i> to the same value for in-place scans. 


### -param pSrcElementFlags [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Compact array of bits with one bit per element of <i>pSrc</i>.  A set value indicates the start of a new segment.


### -param pDst [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Output sequence on the device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



You must point the parameters <i>pSrc</i> and <i>pDst</i> to typed buffers (and not to raw or structured buffers). For information about buffer types, see <a href="https://msdn.microsoft.com/9329f260-e806-4d6d-b6d1-3d001fad411a">Types of Resources</a>. The format of these typed buffers must be <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32_FLOAT</a>, <b>DXGI_FORMAT_R32_UINT</b>, or <b>DXGI_FORMAT_R32_INT</b>. In addition, the format of these typed buffers must match the scan data type that you specify in the <i>ElementType</i> parameter. For example, if the scan data type is <a href="https://msdn.microsoft.com/28bef01c-2d04-48f8-994b-86194f530610">D3DX11_SCAN_DATA_TYPE_UINT</a>, the buffer formats must be <b>DXGI_FORMAT_R32_UINT</b>.

The format of the resource view to which the <i>pSrcElementFlags</i> parameter points must be <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32_UINT</a>.




## -see-also




<a href="https://msdn.microsoft.com/58d8d3ea-25d6-4767-9693-fbc97ae3e8b8">ID3DX11SegmentedScan</a>
 

 

