---
UID: NF:d3dcsx.ID3DX11Scan.Scan
title: ID3DX11Scan::Scan
author: windows-sdk-content
description: Performs an unsegmented scan of a sequence.
old-location: direct3d11\id3dx11scan_scan.htm
old-project: direct3d11
ms.assetid: 42b91efd-3d84-4c76-bb9f-da0f398da6c7
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 4ae96918-c884-060a-690a-7632d7df6622, ID3DX11Scan interface [Direct3D 11],Scan method, ID3DX11Scan.Scan, ID3DX11Scan::Scan, Scan, Scan method [Direct3D 11], Scan method [Direct3D 11],ID3DX11Scan interface, d3dcsx/ID3DX11Scan::Scan, direct3d11.id3dx11scan_scan
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3DX11_SCAN_OPCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11Scan.Scan
product: Windows
targetos: Windows
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
---

# ID3DX11Scan::Scan


## -description


Performs an unsegmented scan of a sequence.


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


### -param pDst [in]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>*</b>

Output sequence on the device.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



You must point the parameters <i>pSrc</i> and <i>pDst</i> to typed buffers (and not to raw or structured buffers). For information about buffer types, see <a href="https://msdn.microsoft.com/9329f260-e806-4d6d-b6d1-3d001fad411a">Types of Resources</a>. The format of these typed buffers must be <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R32_FLOAT</a>, <b>DXGI_FORMAT_R32_UINT</b>, or <b>DXGI_FORMAT_R32_INT</b>. In addition, the format of these typed buffers must match the scan data type that you specify in the <i>ElementType</i> parameter. For example, if the scan data type is <a href="https://msdn.microsoft.com/28bef01c-2d04-48f8-994b-86194f530610">D3DX11_SCAN_DATA_TYPE_UINT</a>, the buffer formats must be <b>DXGI_FORMAT_R32_UINT</b>.




## -see-also




<a href="https://msdn.microsoft.com/f57401b9-fa1e-4470-a974-825749773f95">ID3DX11Scan</a>
 

 

