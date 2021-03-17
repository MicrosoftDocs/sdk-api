---
UID: NF:d3d12.ID3D12Resource.ReadFromSubresource
title: ID3D12Resource::ReadFromSubresource (d3d12.h)
description: Uses the CPU to copy data from a subresource, enabling the CPU to read the contents of most textures with undefined layouts.
helpviewer_keywords: ["ID3D12Resource interface","ReadFromSubresource method","ID3D12Resource.ReadFromSubresource","ID3D12Resource::ReadFromSubresource","ReadFromSubresource","ReadFromSubresource method","ReadFromSubresource method","ID3D12Resource interface","d3d12/ID3D12Resource::ReadFromSubresource","direct3d12.id3d12resource_readfromsubresource"]
old-location: direct3d12\id3d12resource_readfromsubresource.htm
tech.root: direct3d12
ms.assetid: A1F61217-A383-49BF-B675-FBC7F6D015DB
ms.date: 12/05/2018
ms.keywords: ID3D12Resource interface,ReadFromSubresource method, ID3D12Resource.ReadFromSubresource, ID3D12Resource::ReadFromSubresource, ReadFromSubresource, ReadFromSubresource method, ReadFromSubresource method,ID3D12Resource interface, d3d12/ID3D12Resource::ReadFromSubresource, direct3d12.id3d12resource_readfromsubresource
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Resource::ReadFromSubresource
 - d3d12/ID3D12Resource::ReadFromSubresource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Resource.ReadFromSubresource
---

# ID3D12Resource::ReadFromSubresource


## -description

Uses the CPU to copy data from a subresource, enabling the CPU to read the contents of most textures with undefined layouts.

## -parameters

### -param pDstData [out]

Type: <b>void*</b>

A pointer to the destination data in memory.

### -param DstRowPitch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The distance from one row of destination data to the next row.

### -param DstDepthPitch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The distance from one depth slice of destination data to the next.

### -param SrcSubresource

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the index of the subresource to read from.

### -param pSrcBox [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_box">D3D12_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data from.
              If NULL, the data is read from the destination subresource with no offset.
              The dimensions of the destination must fit the destination (see
              <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_box">D3D12_BOX</a>).
            

An empty box results in a no-op.
              A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value.
              When the box is empty, this method doesn't perform any operation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

See the Remarks section for <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">WriteToSubresource</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>



<a href="/windows/desktop/direct3d12/subresources">Subresources</a>