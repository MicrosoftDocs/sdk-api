---
UID: NF:d3d11.ID3D11DeviceContext.CopyStructureCount
title: ID3D11DeviceContext::CopyStructureCount (d3d11.h)
description: Copies data from a buffer holding variable length data.
helpviewer_keywords: ["CopyStructureCount","CopyStructureCount method [Direct3D 11]","CopyStructureCount method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CopyStructureCount method","ID3D11DeviceContext.CopyStructureCount","ID3D11DeviceContext::CopyStructureCount","d3d11/ID3D11DeviceContext::CopyStructureCount","d927d44d-491d-b350-cc6e-49cfd29f1793","direct3d11.id3d11devicecontext_copystructurecount"]
old-location: direct3d11\id3d11devicecontext_copystructurecount.htm
tech.root: direct3d11
ms.assetid: d4f8576f-8d23-4b45-a5ea-099c71e8567e
ms.date: 12/05/2018
ms.keywords: CopyStructureCount, CopyStructureCount method [Direct3D 11], CopyStructureCount method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CopyStructureCount method, ID3D11DeviceContext.CopyStructureCount, ID3D11DeviceContext::CopyStructureCount, d3d11/ID3D11DeviceContext::CopyStructureCount, d927d44d-491d-b350-cc6e-49cfd29f1793, direct3d11.id3d11devicecontext_copystructurecount
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::CopyStructureCount
 - d3d11/ID3D11DeviceContext::CopyStructureCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.CopyStructureCount
---

# ID3D11DeviceContext::CopyStructureCount


## -description

Copies data from a buffer holding variable length data.

## -parameters

### -param pDstBuffer [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

Pointer to <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>.  This can be any buffer resource that other copy commands, 
        such as <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">ID3D11DeviceContext::CopyResource</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">ID3D11DeviceContext::CopySubresourceRegion</a>, are able to write to.

### -param DstAlignedByteOffset [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset from the start of <i>pDstBuffer</i> to write 32-bit UINT structure (vertex) count from <i>pSrcView</i>.

### -param pSrcView [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> of a Structured Buffer resource created with either 
        <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag">D3D11_BUFFER_UAV_FLAG_APPEND</a> or <b>D3D11_BUFFER_UAV_FLAG_COUNTER</b> specified 
        when the UAV was created.   These types of resources have hidden counters tracking "how many" records have 
        been written.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>