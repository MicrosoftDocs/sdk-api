---
UID: NF:d3d12.ID3D12Device8.GetCopyableFootprints1
title: ID3D12Device8::GetCopyableFootprints1
description: Gets a resource layout that can be copied. Helps your app fill in [D3D12_PLACED_SUBRESOURCE_FOOTPRINT](../d3d12/ns-d3d12-d3d12_placed_subresource_footprint.md) and [D3D12_SUBRESOURCE_FOOTPRINT](../d3d12/ns-d3d12-d3d12_subresource_footprint.md) when suballocating space in upload heaps.
helpviewer_keywords: ["ID3D12Device8 interface","GetCopyableFootprints1 method","ID3D12Device8.GetCopyableFootprints1","ID3D12Device8::GetCopyableFootprints1","GetCopyableFootprints1","GetCopyableFootprints1 method","GetCopyableFootprints1 method","ID3D12Device8 interface","direct3d12.id3d12device7_getcopyablefootprints1","d3d12/ID3D12Device8::GetCopyableFootprints1"]
tech.root: direct3d12
ms.date: 09/16/2020
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: d3d12.dll
req.header: d3d12.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: d3d12.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.lib
 - d3d12.dll
api_name:
 - ID3D12Device8::GetCopyableFootprints1
f1_keywords:
 - d3d12/ID3D12Device8::GetCopyableFootprints1
dev_langs:
 - c++
---

## -description

Gets a resource layout that can be copied. Helps your app fill in [D3D12_PLACED_SUBRESOURCE_FOOTPRINT](/windows/win32/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) and [D3D12_SUBRESOURCE_FOOTPRINT](/windows/win32/api/d3d12/ns-d3d12-d3d12_subresource_footprint) when suballocating space in upload heaps.

## -parameters

### -param pResourceDesc

Type: <b>const <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1">D3D12_RESOURCE_DESC1</a>*</b>

A description of the resource, as a pointer to a **D3D12_RESOURCE_DESC1** structure.

### -param FirstSubresource

Type: [in] <b>UINT</b>

Index of the first subresource in the resource. The range of valid values is 0 to D3D12_REQ_SUBRESOURCES.

### -param NumSubresources

Type: [in] <b>UINT</b>

The number of subresources in the resource. The range of valid values is 0 to (D3D12_REQ_SUBRESOURCES - <i>FirstSubresource</i>).

### -param BaseOffset

Type: <b>UINT64</b>

The offset, in bytes, to the resource.

### -param pLayouts

Type: [out, optional] <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>*</b>

A pointer to an array (of length <i>NumSubresources</i>) of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structures, to be filled with the description and placement of each subresource.

### -param pNumRows

Type: [out, optional] <b>UINT*</b>

A pointer to an array (of length <i>NumSubresources</i>) of integer  variables, to be filled with the number of rows for each subresource.

### -param pRowSizeInBytes

Type: [out, optional] <b>UINT64*</b>

A pointer to an array (of length <i>NumSubresources</i>) of integer variables, each entry to be filled with the unpadded size in bytes of a row, of each subresource.

For example, if a Texture2D resource has a width of 32 and bytes per pixel of 4, then <i>pRowSizeInBytes</i> returns 128.

<i>pRowSizeInBytes</i> should not be confused with <b>row pitch</b>, as examining <i>pLayouts</i> and getting the row pitch from that will give you 256 as it is aligned to D3D12_TEXTURE_DATA_PITCH_ALIGNMENT.

### -param pTotalBytes

Type: [out, optional] <b>UINT64*</b>

A pointer to an integer variable, to be filled with the total size, in bytes. If *pResourceDesc* is invalid, then the value of *pTotalBytes* is set to **UINT64_MAX**.

## -remarks

For remarks and examples, see [ID3D12Device::GetCopyableFootprints](./nf-d3d12-id3d12device-getcopyablefootprints.md).

## -see-also

* <a href="/windows/desktop/direct3d12/cd3dx12-resource-desc">CD3DX12_RESOURCE_DESC</a>

* <a href="/windows/desktop/direct3d12/cd3dx12-subresource-footprint">CD3DX12_SUBRESOURCE_FOOTPRINT</a>

* <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>

* [Sampler feedback specification](https://microsoft.github.io/DirectX-Specs/d3d/SamplerFeedback.html)
