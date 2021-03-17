---
UID: NF:d3d10.ID3D10Device.UpdateSubresource
title: ID3D10Device::UpdateSubresource (d3d10.h)
description: The CPU copies data from memory to a subresource created in non-mappable memory. See remarks.
helpviewer_keywords: ["05dfa0e1-63e3-e98a-c07e-e9473eb93d43","ID3D10Device interface [Direct3D 10]","UpdateSubresource method","ID3D10Device.UpdateSubresource","ID3D10Device::UpdateSubresource","UpdateSubresource","UpdateSubresource method [Direct3D 10]","UpdateSubresource method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::UpdateSubresource","direct3d10.id3d10device_updatesubresource"]
old-location: direct3d10\id3d10device_updatesubresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_updatesubresource.htm
ms.date: 12/05/2018
ms.keywords: 05dfa0e1-63e3-e98a-c07e-e9473eb93d43, ID3D10Device interface [Direct3D 10],UpdateSubresource method, ID3D10Device.UpdateSubresource, ID3D10Device::UpdateSubresource, UpdateSubresource, UpdateSubresource method [Direct3D 10], UpdateSubresource method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::UpdateSubresource, direct3d10.id3d10device_updatesubresource
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::UpdateSubresource
 - d3d10/ID3D10Device::UpdateSubresource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.UpdateSubresource
---

# ID3D10Device::UpdateSubresource


## -description

The CPU copies data from memory to a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> created in non-mappable memory. See remarks.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

A pointer to the destination resource (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource Interface</a>).

### -param DstSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index, that identifies the destination subresource. See <a href="/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> for more details.

### -param pDstBox [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_box">D3D10_BOX</a>*</b>

A box that defines the portion of the destination subresource to copy the resource data into. Coordinates are in bytes for buffers and in texels for textures. If <b>NULL</b>, the data is written to the destination subresource with no offset. The dimensions of the source must fit the destination (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_box">D3D10_BOX</a>).

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>UpdateSubresource</b> doesn't perform an update operation.

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

For a shader-constant buffer; set pDstBox to <b>NULL</b>. It is not possible to use this method to partially update a shader-constant buffer.

A resource cannot be used as a destination if:

<ul>
<li>the resource is created with <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">immutable</a> or <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">dynamic</a> usage.</li>
<li>the resource is created as a <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil resource</a>.</li>
<li>the resource is created with multisampling capability (see <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a>).</li>
</ul>
When UpdateSubresource returns, the application is free to change or even free the data pointed to by pSrcData because the method has already copied/snapped away the original contents.

The performance of UpdateSubresource depends on whether or not there is contention for the destination resource. For example, contention for a vertex buffer resource occurs when the application executes a Draw call and later calls UpdateSubresource on the same vertex buffer before the Draw call is actually executed by the GPU.

<ul>
<li>When there is contention for the resource, UpdateSubresource will perform 2 copies of the source data. First, the data is copied by the CPU to a temporary storage space accessible by the command buffer. This copy happens before the method returns.  A second copy is then performed by the GPU to copy the source data into non-mappable memory. This second copy happens asynchronously because it is executed by GPU when the command buffer is flushed.</li>
<li>When there is no resource contention, the behavior of UpdateSubresource is dependent on which is faster (from the CPU's perspective): copying the data to the command buffer and then having a second copy execute when the command buffer is flushed, or having the CPU copy the data to the final resource location. This is dependent on the architecture of the underlying system.</li>
</ul>
To better understand the source row pitch and source depth pitch parameters, consider the following illustration of a 3D volume texture.

<img alt="Illustration of a 3D volume texture" src="./images/d3d10_pitches_conceptual.png"/>

Each block in this visual represents an element of data, and the size of each element is dependent on the resource's format. For example, if the resource format is DXGI_FORMAT_R32G32B32A32_FLOAT, then the size of each element would be 128 bits, or 16 bytes. This 3D volume texture has a width of two, a height of three, and a depth of four.

To calculate the source row pitch and source depth pitch for a given resource, use the following formulas:

<ul>
<li>Source Row Pitch = [size of one element in bytes] * [number of elements in one row]</li>
<li>Source Depth Pitch = [Source Row Pitch] * [number of rows (height)]</li>
</ul>
In the case of this example 3D volume texture where the size of each element is 16 bytes, the formulas are as follows:

<ul>
<li>Source Row Pitch = 16 * 2 = 32</li>
<li>Source Depth Pitch = 16 * 2 * 3 = 96</li>
</ul>
The following illustration shows the resource as it is laid out in memory.

<img alt="Illustration of a 3D volume texture in memory" src="./images/d3d10_pitches.png"/>

For example, the following code snippet shows how to specify a destination region in a 2D texture. Assume the destination texture is 512x512 and the operation will copy the data pointed to by pData to  [(120,100)..(200,220)] in the destination texture. Also assume that rowPitch has been initialized with the proper value (as explained above). Front and back are set to 0 and 1 respectively, because by having front equal to back, the box is technically empty.


```

D3D10_BOX destRegion;
destRegion.left = 120;
destRegion.right = 200;
destRegion.top = 100;
destRegion.bottom = 220;
destRegion.front = 0;
destRegion.back = 1;

pd3dDevice->UpdateSubresource( pDestTexture, 0, &destRegion, pData, rowPitch, 0 );

```


The 1D case is similar. The following snippet shows how to specify a destination region in a 1D texture. Use the same assumptions as above, except that the texture is 512 in length.


```

D3D10_BOX destRegion;
destRegion.left = 120;
destRegion.right = 200;
destRegion.top = 0;
destRegion.bottom = 1;
destRegion.front = 0;
destRegion.back = 1;

pd3dDevice->UpdateSubresource( pDestTexture, 0, &destRegion, pData, rowPitch, 0 );

```


<table>
<tr>
<td>
Differences between Direct3D 10 and Direct3D 10.1:

Direct3D 10.1 enables depth-stencil resources to be used as either a source or destination.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource Interface</a>