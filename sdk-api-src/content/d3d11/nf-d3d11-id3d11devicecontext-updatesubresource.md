---
UID: NF:d3d11.ID3D11DeviceContext.UpdateSubresource
title: ID3D11DeviceContext::UpdateSubresource (d3d11.h)
description: The CPU copies data from memory to a subresource created in non-mappable memory. (ID3D11DeviceContext.UpdateSubresource)
helpviewer_keywords: ["ID3D11DeviceContext interface [Direct3D 11]","UpdateSubresource method","ID3D11DeviceContext.UpdateSubresource","ID3D11DeviceContext::UpdateSubresource","UpdateSubresource","UpdateSubresource method [Direct3D 11]","UpdateSubresource method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::UpdateSubresource","direct3d11.id3d11devicecontext_updatesubresource","f9813ce8-3ca5-fd5e-fac2-bd93631ecbc8"]
old-location: direct3d11\id3d11devicecontext_updatesubresource.htm
tech.root: direct3d11
ms.assetid: 2d8ef5a2-204a-434d-918a-104419050233
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],UpdateSubresource method, ID3D11DeviceContext.UpdateSubresource, ID3D11DeviceContext::UpdateSubresource, UpdateSubresource, UpdateSubresource method [Direct3D 11], UpdateSubresource method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::UpdateSubresource, direct3d11.id3d11devicecontext_updatesubresource, f9813ce8-3ca5-fd5e-fac2-bd93631ecbc8
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
 - ID3D11DeviceContext::UpdateSubresource
 - d3d11/ID3D11DeviceContext::UpdateSubresource
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
 - ID3D11DeviceContext.UpdateSubresource
---

## -description

See the [Basic hologram sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/BasicHologram).

The CPU copies data from memory to a subresource created in non-mappable memory.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the destination resource (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>).

### -param DstSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index, that identifies the destination subresource. See <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11calcsubresource">D3D11CalcSubresource</a> for more details.

### -param pDstBox [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_box">D3D11_BOX</a>*</b>

A pointer to a box that defines the portion of the destination subresource to copy the resource data into. Coordinates are in bytes for buffers and in texels for textures. If <b>NULL</b>, the data is written to the destination subresource with no offset. The dimensions of the source must fit the destination (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_box">D3D11_BOX</a>).

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

For a shader-constant buffer; set <i>pDstBox</i> to <b>NULL</b>. It is not possible to use this method to partially update a shader-constant buffer.

A resource cannot be used as a destination if:

<ul>
<li>the resource is created with <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">immutable</a> or <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">dynamic</a> usage.</li>
<li>the resource is created as a depth-stencil resource.</li>
<li>the resource is created with multisampling capability (see <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a>).</li>
</ul>
When <b>UpdateSubresource</b> returns, the application is free to change or even free the data pointed to by <i>pSrcData</i> because the method has already copied/snapped away the original contents.

The performance of <b>UpdateSubresource</b> depends on whether or not there is contention for the destination resource. For example, contention for a vertex buffer resource occurs when the application executes a <b>Draw</b> call and later calls <b>UpdateSubresource</b> on the same vertex buffer before the <b>Draw</b> call is actually executed by the GPU.

<ul>
<li>When there is contention for the resource, <b>UpdateSubresource</b> will perform 2 copies of the source data. First, the data is copied by the CPU to a temporary storage space accessible by the command buffer. This copy happens before the method returns.  A second copy is then performed by the GPU to copy the source data into non-mappable memory. This second copy happens asynchronously because it is executed by GPU when the command buffer is flushed.</li>
<li>When there is no resource contention, the behavior of <b>UpdateSubresource</b> is dependent on which is faster (from the CPU's perspective): copying the data to the command buffer and then having a second copy execute when the command buffer is flushed, or having the CPU copy the data to the final resource location. This is dependent on the architecture of the underlying system.</li>
</ul>
<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <b>UpdateSubresource</b> or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">ID3D11DeviceContext::CopySubresourceRegion</a> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>
To better understand the source row pitch and source depth pitch parameters, the following illustration shows a 3D volume texture.

<img alt="Illustration of a 3D volume texture" src="./images/D3D10_pitches_conceptual.png"/>

Each block in this visual represents an element of data, and the size of each element is dependent on the resource's format. For example, if the resource format is DXGI_FORMAT_R32G32B32A32_FLOAT, the size of each element would be 128 bits, or 16 bytes. This 3D volume texture has a width of two, a height of three, and a depth of four.

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

<img alt="Illustration of a 3D volume texture laid out in memory" src="./images/D3D10_pitches.png"/>

For example, the following code snippet shows how to specify a destination region in a 2D texture. Assume the destination texture is 512x512 and the operation will copy the data pointed to by <i>pData</i> to  [(120,100)..(200,220)] in the destination texture. Also assume that <i>rowPitch</i> has been initialized with the proper value (as explained above). <b>front</b> and <b>back</b> are set to 0 and 1 respectively, because by having <b>front</b> equal to <b>back</b>, the box is technically empty.


```

D3D11_BOX destRegion;
destRegion.left = 120;
destRegion.right = 200;
destRegion.top = 100;
destRegion.bottom = 220;
destRegion.front = 0;
destRegion.back = 1;

pd3dDeviceContext->UpdateSubresource( pDestTexture, 0, &destRegion, pData, rowPitch, 0 );

```


The 1D case is similar. The following snippet shows how to specify a destination region in a 1D texture. Use the same assumptions as above, except that the texture is 512 in length.


```

D3D11_BOX destRegion;
destRegion.left = 120;
destRegion.right = 200;
destRegion.top = 0;
destRegion.bottom = 1;
destRegion.front = 0;
destRegion.back = 1;

pd3dDeviceContext->UpdateSubresource( pDestTexture, 0, &destRegion, pData, rowPitch, 0 );

```


For info about various resource types and how <b>UpdateSubresource</b> might work with each resource type, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro">Introduction to a Resource in Direct3D 11</a>. 

<h3><a id="Calling_UpdateSubresource_on_a_Deferred_Context"></a><a id="calling_updatesubresource_on_a_deferred_context"></a><a id="CALLING_UPDATESUBRESOURCE_ON_A_DEFERRED_CONTEXT"></a>Calling UpdateSubresource on a Deferred Context</h3>
If your application calls <b>UpdateSubresource</b> on a deferred context with a destination box—to which <i>pDstBox</i> points—that has a non-(0,0,0) offset, and if the driver does not support command lists, <b>UpdateSubresource</b> inappropriately applies that destination-box offset to the <i>pSrcData</i> parameter. To work around this behavior, use the following code:


```

HRESULT UpdateSubresource_Workaround(
  ID3D11Device *pDevice,
  ID3D11DeviceContext *pDeviceContext,
  ID3D11Resource *pDstResource,
  UINT dstSubresource,
  const D3D11_BOX *pDstBox,
  const void *pSrcData,
  UINT srcBytesPerElement,
  UINT srcRowPitch,
  UINT srcDepthPitch,
  bool* pDidWorkAround )
{
     HRESULT hr = S_OK;
     bool needWorkaround = false;
     D3D11_DEVICE_CONTEXT_TYPE contextType = pDeviceContext->GetType();

     if( pDstBox && (D3D11_DEVICE_CONTEXT_DEFERRED == contextType) )
     {
          D3D11_FEATURE_DATA_THREADING threadingCaps = { FALSE, FALSE };

          hr = pDevice->CheckFeatureSupport( D3D11_FEATURE_THREADING, &threadingCaps, sizeof(threadingCaps) );
          if( SUCCEEDED(hr) )
          {
               if( !threadingCaps.DriverCommandLists )
               {
                    needWorkaround = true;
               }
          }
     }

     const void* pAdjustedSrcData = pSrcData;

     if( needWorkaround )
     {
          D3D11_BOX alignedBox = *pDstBox;
		
          // convert from pixels to blocks
          if( m_bBC )
          {
               alignedBox.left     /= 4;
               alignedBox.right    /= 4;
               alignedBox.top      /= 4;
               alignedBox.bottom   /= 4;
          }

          pAdjustedSrcData = ((const BYTE*)pSrcData) - (alignedBox.front * srcDepthPitch) - (alignedBox.top * srcRowPitch) - (alignedBox.left * srcBytesPerElement);
     }

     pDeviceContext->UpdateSubresource( pDstResource, dstSubresource, pDstBox, pAdjustedSrcData, srcRowPitch, srcDepthPitch );

     if( pDidWorkAround )
     {
          *pDidWorkAround = needWorkaround;
     }

     return hr;
}

```

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>

[Basic hologram sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/BasicHologram)
