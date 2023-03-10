---
UID: NF:d3d12.ID3D12GraphicsCommandList.CopyTextureRegion
title: ID3D12GraphicsCommandList::CopyTextureRegion (d3d12.h)
description: This method uses the GPU to copy texture data between two locations. Both the source and the destination may reference texture data located within either a buffer resource or a texture resource.
helpviewer_keywords: ["CopyTextureRegion","CopyTextureRegion method","CopyTextureRegion method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","CopyTextureRegion method","ID3D12GraphicsCommandList.CopyTextureRegion","ID3D12GraphicsCommandList::CopyTextureRegion","d3d12/ID3D12GraphicsCommandList::CopyTextureRegion","direct3d12.id3d12graphicscommandlist_copytextureregion"]
old-location: direct3d12\id3d12graphicscommandlist_copytextureregion.htm
tech.root: direct3d12
ms.assetid: 2EAFC6B9-376C-4801-8E53-BF0DB08943AA
ms.date: 12/05/2018
ms.keywords: CopyTextureRegion, CopyTextureRegion method, CopyTextureRegion method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,CopyTextureRegion method, ID3D12GraphicsCommandList.CopyTextureRegion, ID3D12GraphicsCommandList::CopyTextureRegion, d3d12/ID3D12GraphicsCommandList::CopyTextureRegion, direct3d12.id3d12graphicscommandlist_copytextureregion
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
 - ID3D12GraphicsCommandList::CopyTextureRegion
 - d3d12/ID3D12GraphicsCommandList::CopyTextureRegion
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
 - ID3D12GraphicsCommandList.CopyTextureRegion
---

# ID3D12GraphicsCommandList::CopyTextureRegion


## -description

This method uses the GPU to copy texture data between two locations. Both the source and the destination may reference texture data located within either a buffer resource or a texture resource.

## -parameters

### -param pDst [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a>*</b>

Specifies the destination <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a>. The subresource referred to must be in the D3D12_RESOURCE_STATE_COPY_DEST state.

### -param DstX

Type: <b>UINT</b>

The x-coordinate of the upper left corner of the destination region.

### -param DstY

Type: <b>UINT</b>

The y-coordinate of the upper left corner of the destination region. For a 1D subresource, this must be zero.

### -param DstZ

Type: <b>UINT</b>

The z-coordinate of the upper left corner of the destination region. For a 1D or 2D subresource, this must be zero.

### -param pSrc [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a>*</b>

Specifies the source <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a>.
          The subresource referred to must be in the D3D12_RESOURCE_STATE_COPY_SOURCE state.

### -param pSrcBox [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_box">D3D12_BOX</a>*</b>

Specifies an optional  D3D12_BOX that sets the size of the source texture to copy.

## -remarks

The source box must be within the size of the source resource. The destination offsets, (x, y, and z), allow the source box to be offset when writing into the destination resource; however, the dimensions of the source box and the offsets must be within the size of the resource. If you try and copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of <b>CopyTextureRegion</b> is undefined. If you created a device that supports the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a>, the debug output reports an error on this invalid <b>CopyTextureRegion</b> call. Invalid parameters to <b>CopyTextureRegion</b> cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.
        

If the resources are buffers, all coordinates are in bytes; if the resources are textures, all coordinates are in texels. 

<b>CopyTextureRegion</b> performs the copy on the GPU (similar to a <code>memcpy</code> by the CPU). As a consequence, the source and destination resources:
        

<ul>
<li>Must be different subresources (although they can be from the same resource).</li>
<li>Must have compatible <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>s (identical or from the same type group). For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to a DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. <b>CopyTextureRegion</b> can copy between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.</li>
</ul>
<b>CopyTextureRegion</b> only supports copy; it does not support any stretch, color key, or blend. <b>CopyTextureRegion</b> can reinterpret the resource data between a few format types.

Note that for a depth-stencil buffer, the depth and stencil planes are <a href="/windows/win32/direct3d12/subresources#plane-slice">separate subresources</a> within the buffer.

To copy an entire resource, rather than just a region of a subresource, we recommend to use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource">CopyResource</a> instead.

<div class="alert"><b>Note</b>  If you use <b>CopyTextureRegion</b> with a depth-stencil buffer or a multisampled resource, you must copy the entire subresource rectangle. In this situation, you must pass 0 to the <i>DstX</i>, <i>DstY</i>, and <i>DstZ</i> parameters and <b>NULL</b> to the <i>pSrcBox</i> parameter. In addition, source and destination resources, which are represented by the <i>pSrcResource</i> and <i>pDstResource</i> parameters, should have identical sample count values.
        </div>
<div> </div>
<b>CopyTextureRegion</b> may be used to initialize resources which alias the same heap memory. See <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a> for more details.

<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following code snippet copies the box (located at (120,100),(200,220)) from a source texture into the region (10,20),(90,140) in a destination texture.


```
D3D12_BOX sourceRegion;
sourceRegion.left = 120;
sourceRegion.top = 100;
sourceRegion.right = 200;
sourceRegion.bottom = 220;
sourceRegion.front = 0;
sourceRegion.back = 1;

pCmdList -> CopyTextureRegion(pDestTexture, 10, 20, 0, pSourceTexture, &sourceRegion);

```


Notice, that for a 2D texture, front and back are set to 0 and 1 respectively.


#### Examples

The <b>HelloTriangle</b> sample uses <b>ID3D12GraphicsCommandList::CopyTextureRegion</b> as follows:
        


```cpp
inline UINT64 UpdateSubresources(
    _In_ ID3D12GraphicsCommandList* pCmdList,
    _In_ ID3D12Resource* pDestinationResource,
    _In_ ID3D12Resource* pIntermediate,
    _In_range_(0,D3D12_REQ_SUBRESOURCES) UINT FirstSubresource,
    _In_range_(0,D3D12_REQ_SUBRESOURCES-FirstSubresource) UINT NumSubresources,
    UINT64 RequiredSize,
    _In_reads_(NumSubresources) const D3D12_PLACED_SUBRESOURCE_FOOTPRINT* pLayouts,
    _In_reads_(NumSubresources) const UINT* pNumRows,
    _In_reads_(NumSubresources) const UINT64* pRowSizesInBytes,
    _In_reads_(NumSubresources) const D3D12_SUBRESOURCE_DATA* pSrcData)
{
    // Minor validation
    D3D12_RESOURCE_DESC IntermediateDesc = pIntermediate->GetDesc();
    D3D12_RESOURCE_DESC DestinationDesc = pDestinationResource->GetDesc();
    if (IntermediateDesc.Dimension != D3D12_RESOURCE_DIMENSION_BUFFER || 
        IntermediateDesc.Width < RequiredSize + pLayouts[0].Offset || 
        RequiredSize > (SIZE_T)-1 || 
        (DestinationDesc.Dimension == D3D12_RESOURCE_DIMENSION_BUFFER && 
            (FirstSubresource != 0 || NumSubresources != 1)))
    {
        return 0;
    }
    
    BYTE* pData;
    HRESULT hr = pIntermediate->Map(0, NULL, reinterpret_cast<void**>(&pData));
    if (FAILED(hr))
    {
        return 0;
    }
    
    for (UINT i = 0; i < NumSubresources; ++i)
    {
        if (pRowSizesInBytes[i] > (SIZE_T)-1) return 0;
        D3D12_MEMCPY_DEST DestData = { pData + pLayouts[i].Offset, pLayouts[i].Footprint.RowPitch, pLayouts[i].Footprint.RowPitch * pNumRows[i] };
        MemcpySubresource(&DestData, &pSrcData[i], (SIZE_T)pRowSizesInBytes[i], pNumRows[i], pLayouts[i].Footprint.Depth);
    }
    pIntermediate->Unmap(0, NULL);
    
    if (DestinationDesc.Dimension == D3D12_RESOURCE_DIMENSION_BUFFER)
    {
        CD3DX12_BOX SrcBox( UINT( pLayouts[0].Offset ), UINT( pLayouts[0].Offset + pLayouts[0].Footprint.Width ) );
        pCmdList->CopyBufferRegion(
            pDestinationResource, 0, pIntermediate, pLayouts[0].Offset, pLayouts[0].Footprint.Width);
    }
    else
    {
        for (UINT i = 0; i < NumSubresources; ++i)
        {
            CD3DX12_TEXTURE_COPY_LOCATION Dst(pDestinationResource, i + FirstSubresource);
            CD3DX12_TEXTURE_COPY_LOCATION Src(pIntermediate, pLayouts[i]);
            pCmdList->CopyTextureRegion(&Dst, 0, 0, 0, &Src, nullptr);
        }
    }
    return RequiredSize;
}

```


See <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.
        

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion">CopyBufferRegion</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>