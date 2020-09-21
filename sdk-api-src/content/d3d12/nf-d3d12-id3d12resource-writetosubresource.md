---
UID: NF:d3d12.ID3D12Resource.WriteToSubresource
title: ID3D12Resource::WriteToSubresource (d3d12.h)
description: Uses the CPU to copy data into a subresource, enabling the CPU to modify the contents of most textures with undefined layouts.
helpviewer_keywords: ["ID3D12Resource interface","WriteToSubresource method","ID3D12Resource.WriteToSubresource","ID3D12Resource::WriteToSubresource","WriteToSubresource","WriteToSubresource method","WriteToSubresource method","ID3D12Resource interface","d3d12/ID3D12Resource::WriteToSubresource","direct3d12.id3d12resource_writetosubresource"]
old-location: direct3d12\id3d12resource_writetosubresource.htm
tech.root: direct3d12
ms.assetid: 8781E2FE-8D82-41F5-B541-A96DA11CA290
ms.date: 12/05/2018
ms.keywords: ID3D12Resource interface,WriteToSubresource method, ID3D12Resource.WriteToSubresource, ID3D12Resource::WriteToSubresource, WriteToSubresource, WriteToSubresource method, WriteToSubresource method,ID3D12Resource interface, d3d12/ID3D12Resource::WriteToSubresource, direct3d12.id3d12resource_writetosubresource
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
 - ID3D12Resource::WriteToSubresource
 - d3d12/ID3D12Resource::WriteToSubresource
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
 - ID3D12Resource.WriteToSubresource
---

# ID3D12Resource::WriteToSubresource


## -description

Uses the CPU to copy data into a subresource, enabling the CPU to modify the contents of most textures with undefined layouts.

## -parameters

### -param DstSubresource

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the index of the subresource.

### -param pDstBox [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_box">D3D12_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data into.
              If NULL, the data is written to the destination subresource with no offset.
              The dimensions of the source must fit the destination (see
              <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_box">D3D12_BOX</a>).
            

An empty box results in a no-op.
              A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, 
				  or the front value is greater than or equal to the back value.
              When the box is empty, this method doesn't perform any operation.

### -param pSrcData [in]

Type: <b>const void*</b>

A pointer to the source data in memory.

### -param SrcRowPitch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The distance from one row of source data to the next row.

### -param SrcDepthPitch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The distance from one depth slice of source data to the next.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

The resource should first be mapped using
          <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map">Map</a>. Textures must be in the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_COMMON</a> state for CPU access through <b>WriteToSubresource</b> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource">ReadFromSubresource</a> to be legal; but buffers do not.

For efficiency, ensure the bounds and alignment of the extents within the box are ( 64 / [bytes per pixel] ) pixels horizontally.
          Vertical bounds and alignment should be 2 rows, except when 1-byte-per-pixel formats are used, in which case 4 rows are recommended.
          Single depth slices per call are handled efficiently.
          It is recommended but not necessary to provide pointers and strides which are 128-byte aligned.
        

When writing to sub mipmap levels, it is recommended to use larger width and heights than described above.
          This is because small mipmap levels may actually be stored within a larger block of memory, with an opaque amount of offsetting which can interfere with alignment to cache lines.
        

<b>WriteToSubresource</b> and <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource">ReadFromSubresource</a> enable near zero-copy optimizations for UMA adapters, but can prohibitively impair the efficiency of discrete/ NUMA adapters as the texture data cannot reside in local video memory. Typical applications should stick to discrete-friendly upload techniques, unless they recognize the adapter architecture is UMA. For more details on uploading, refer to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a>, and for more details on UMA, refer to <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture">D3D12_FEATURE_DATA_ARCHITECTURE</a>. 

On UMA systems, this routine can be used to minimize the cost of memory copying through the loop optimization known as <a href="https://en.wikipedia.org/wiki/Loop_tiling">loop tiling</a>. By breaking up the upload into chucks that comfortably fit in the CPU cache, the effective bandwidth between the CPU and main memory more closely achieves theoretical maximums.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>



<a href="/windows/desktop/direct3d12/subresources">Subresources</a>