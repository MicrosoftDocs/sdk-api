---
UID: NF:d3d12.ID3D12Device.GetCopyableFootprints
title: ID3D12Device::GetCopyableFootprints (d3d12.h)
description: Gets a resource layout that can be copied. Helps the app fill-in D3D12_PLACED_SUBRESOURCE_FOOTPRINT and D3D12_SUBRESOURCE_FOOTPRINT when suballocating space in upload heaps.
helpviewer_keywords: ["GetCopyableFootprints","GetCopyableFootprints method","GetCopyableFootprints method","ID3D12Device interface","ID3D12Device interface","GetCopyableFootprints method","ID3D12Device.GetCopyableFootprints","ID3D12Device::GetCopyableFootprints","d3d12/ID3D12Device::GetCopyableFootprints","direct3d12.id3d12device_getcopyablefootprints"]
old-location: direct3d12\id3d12device_getcopyablefootprints.htm
tech.root: direct3d12
ms.assetid: EB3715A9-5A73-45DA-A46F-7889188409A3
ms.date: 12/05/2018
ms.keywords: GetCopyableFootprints, GetCopyableFootprints method, GetCopyableFootprints method,ID3D12Device interface, ID3D12Device interface,GetCopyableFootprints method, ID3D12Device.GetCopyableFootprints, ID3D12Device::GetCopyableFootprints, d3d12/ID3D12Device::GetCopyableFootprints, direct3d12.id3d12device_getcopyablefootprints
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
 - ID3D12Device::GetCopyableFootprints
 - d3d12/ID3D12Device::GetCopyableFootprints
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
 - ID3D12Device.GetCopyableFootprints
---

# ID3D12Device::GetCopyableFootprints


## -description

Gets a resource layout that can be copied.
          Helps the app fill-in 
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and 
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint">D3D12_SUBRESOURCE_FOOTPRINT</a> when suballocating space in upload heaps.

## -parameters

### -param pResourceDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a>*</b>

A description of the resource, as a pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> structure.

### -param FirstSubresource [in]

Type: <b>UINT</b>

Index of the first subresource in the resource.
            The range of valid values is 0 to D3D12_REQ_SUBRESOURCES.

### -param NumSubresources [in]

Type: <b>UINT</b>

The number of subresources in the resource.  The range of valid values is 0 to (D3D12_REQ_SUBRESOURCES - <i>FirstSubresource</i>).

### -param BaseOffset

Type: <b>UINT64</b>

The offset, in bytes, to the resource.

### -param pLayouts [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a>*</b>

A pointer to an array (of length <i>NumSubresources</i>) of
            <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structures, to be filled with the description and placement of each subresource.

### -param pNumRows [out, optional]

Type: <b>UINT*</b>

A pointer to an array (of length <i>NumSubresources</i>) of integer  variables, to be filled with the number of rows for each subresource.

### -param pRowSizeInBytes [out, optional]

Type: <b>UINT64*</b>

A pointer to an array (of length <i>NumSubresources</i>) of integer variables, each entry to be filled with the unpadded size in bytes of a row, of each subresource.
          

For example, if a Texture2D resource has a width of 32 and bytes per pixel of 4, 

then <i>pRowSizeInBytes</i> returns 128.

<i>pRowSizeInBytes</i> should not be confused with <b>row pitch</b>, as examining <i>pLayouts</i> and getting the row pitch from that will give you 256 as it is aligned to D3D12_TEXTURE_DATA_PITCH_ALIGNMENT.

### -param pTotalBytes [out, optional]

Type: <b>UINT64*</b>

A pointer to an integer variable, to be filled with the total size, in bytes. If *pResourceDesc* is invalid, then the value of *pTotalBytes* is set to **UINT64_MAX**.

## -remarks

This routine assists the application in filling out
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> and
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint">D3D12_SUBRESOURCE_FOOTPRINT</a> structures, when suballocating space in upload heaps.
          The resulting structures are GPU adapter-agnostic, meaning that the values will not vary from one GPU adapter to the next.
          <b>GetCopyableFootprints</b> uses specified details about resource formats, texture layouts, and alignment requirements (from the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> structure)  to fill out the subresource structures.
          Applications have access to all these details, so this method, or a variation of it, could be  written as part of the app.
        


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12Multithreading</a> sample uses <b>ID3D12Device::GetCopyableFootprints</b> as follows:
        


```cpp
// Returns required size of a buffer to be used for data upload
inline UINT64 GetRequiredIntermediateSize(
    _In_ ID3D12Resource* pDestinationResource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources)
{
    D3D12_RESOURCE_DESC Desc = pDestinationResource->GetDesc();
    UINT64 RequiredSize = 0;
    
    ID3D12Device* pDevice;
    pDestinationResource->GetDevice(__uuidof(*pDevice), reinterpret_cast<void**>(&pDevice));
    pDevice->GetCopyableFootprints(&Desc, FirstSubresource, NumSubresources, 0, nullptr, nullptr, nullptr, &RequiredSize);
    pDevice->Release();
    
    return RequiredSize;
}

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
          

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc">CD3DX12_RESOURCE_DESC</a>



<a href="/windows/desktop/direct3d12/cd3dx12-subresource-footprint">CD3DX12_SUBRESOURCE_FOOTPRINT</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>