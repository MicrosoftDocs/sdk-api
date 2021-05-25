---
UID: NF:d3d11_3.ID3D11Device3.WriteToSubresource
title: ID3D11Device3::WriteToSubresource (d3d11_3.h)
description: Copies data into a D3D11_USAGE_DEFAULTtexture which was mapped using ID3D11DeviceContext3::Mapwhile providing a NULL D3D11_MAPPED_SUBRESOURCEparameter.
helpviewer_keywords: ["ID3D11Device3 interface [Direct3D 11]","WriteToSubresource method","ID3D11Device3.WriteToSubresource","ID3D11Device3::WriteToSubresource","WriteToSubresource","WriteToSubresource method [Direct3D 11]","WriteToSubresource method [Direct3D 11]","ID3D11Device3 interface","d3d11_3/ID3D11Device3::WriteToSubresource","direct3d11.id3d11device3_writetosubresource"]
old-location: direct3d11\id3d11device3_writetosubresource.htm
tech.root: direct3d11
ms.assetid: DCA4A88D-3DCA-41D5-AE52-061A605A9CBF
ms.date: 12/05/2018
ms.keywords: ID3D11Device3 interface [Direct3D 11],WriteToSubresource method, ID3D11Device3.WriteToSubresource, ID3D11Device3::WriteToSubresource, WriteToSubresource, WriteToSubresource method [Direct3D 11], WriteToSubresource method [Direct3D 11],ID3D11Device3 interface, d3d11_3/ID3D11Device3::WriteToSubresource, direct3d11.id3d11device3_writetosubresource
req.header: d3d11_3.h
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
 - ID3D11Device3::WriteToSubresource
 - d3d11_3/ID3D11Device3::WriteToSubresource
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
 - ID3D11Device3.WriteToSubresource
---

# ID3D11Device3::WriteToSubresource


## -description

Copies data into a
          <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DEFAULT</a> texture which was mapped using
          ID3D11DeviceContext3::<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">Map</a> while providing a NULL
          <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_mapped_subresource">D3D11_MAPPED_SUBRESOURCE</a> parameter.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the destination resource (an
            <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>).

### -param DstSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index, that identifies the destination subresource.
            For more details, see
            <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11calcsubresource">D3D11CalcSubresource</a>.

### -param pDstBox [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_box">D3D11_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data into.
              If NULL, the data is written to the destination subresource with no offset.
              The dimensions of the source must fit the destination (see
              <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_box">D3D11_BOX</a>).
            

An empty box results in a no-op.
              A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value.
              When the box is empty, this method doesn't perform any operation.

### -param pSrcData [in]

Type: <b>const void*</b>

A pointer to the source data in memory.

### -param SrcRowPitch [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of one row of the source data.

### -param SrcDepthPitch [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of one depth slice of source data.

## -remarks

The provided resource must be a
          <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">D3D11_USAGE_DEFAULT</a> texture which was mapped for writing by a previous call to
          ID3D11DeviceContext3::<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">Map</a> while providing a NULL
          <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_mapped_subresource">D3D11_MAPPED_SUBRESOURCE</a> parameter.
        

This API is intended for calling at high frequency.
          Callers can reduce memory by making iterative calls that update progressive regions of the texture, while provide a small buffer during each call.
          It is most efficient to specify large enough regions, though, because this enables D3D to fill whole cache lines in the texture before returning.
        

For efficiency, ensure the bounds and alignment of the extents within the box are ( 64 / [bytes per pixel] ) pixels horizontally.
          Vertical bounds and alignment should be 2 rows, except when 1-byte-per-pixel formats are used, in which case 4 rows are recommended.
          Single depth slices per call are handled efficiently.
          It is recommended but not necessary to provide pointers and strides which are 128-byte aligned.
        

When writing to sub mipmap levels, it is recommended to use larger width and heights than described above.
          This is because small mipmap levels may actually be stored within a larger block of memory, with an opaque amount of offsetting which can interfere with alignment to cache lines.

## -see-also

<a href="/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11device3">ID3D11Device3</a>