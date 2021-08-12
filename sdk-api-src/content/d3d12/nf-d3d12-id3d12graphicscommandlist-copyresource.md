---
UID: NF:d3d12.ID3D12GraphicsCommandList.CopyResource
title: ID3D12GraphicsCommandList::CopyResource (d3d12.h)
description: Copies the entire contents of the source resource to the destination resource.
helpviewer_keywords: ["CopyResource","CopyResource method","CopyResource method","ID3D12GraphicsCommandList interface","ID3D12GraphicsCommandList interface","CopyResource method","ID3D12GraphicsCommandList.CopyResource","ID3D12GraphicsCommandList::CopyResource","d3d12/ID3D12GraphicsCommandList::CopyResource","direct3d12.id3d12graphicscommandlist_copyresource"]
old-location: direct3d12\id3d12graphicscommandlist_copyresource.htm
tech.root: direct3d12
ms.assetid: EFC305CF-FBA9-4192-999B-6C6BFCDFF51F
ms.date: 12/05/2018
ms.keywords: CopyResource, CopyResource method, CopyResource method,ID3D12GraphicsCommandList interface, ID3D12GraphicsCommandList interface,CopyResource method, ID3D12GraphicsCommandList.CopyResource, ID3D12GraphicsCommandList::CopyResource, d3d12/ID3D12GraphicsCommandList::CopyResource, direct3d12.id3d12graphicscommandlist_copyresource
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
 - ID3D12GraphicsCommandList::CopyResource
 - d3d12/ID3D12GraphicsCommandList::CopyResource
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
 - ID3D12GraphicsCommandList.CopyResource
---

# ID3D12GraphicsCommandList::CopyResource


## -description

Copies the entire contents of the source resource to the destination resource.

## -parameters

### -param pDstResource [in]

Type: <b>ID3D12Resource*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface that represents the destination resource.

### -param pSrcResource [in]

Type: <b>ID3D12Resource*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> interface that represents the source resource.

## -remarks

<b>CopyResource</b> operations are performed on the GPU and do not incur a significant CPU workload linearly dependent on the size of the data to copy.
        

<b>CopyResource</b> may be used to initialize resources which alias the same heap memory. See <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">CreatePlacedResource</a> for more details.

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue an error if the source subresource is not in the  <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_COPY_SOURCE</a> state.
          

The debug layer will issue an error if the destination subresource is not in the  <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_COPY_DEST </a> state.
          

This method has a few restrictions designed for improving performance. For instance, the source and destination resources:

<ul>
<li>Must be different resources.</li>
<li>Must be the same type.</li>
<li>Must have identical dimensions (including width, height, depth, and size as appropriate).</li>
<li>Must have compatible <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI formats</a>, which means the formats must be identical or at least from the same type group. For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to a DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. <b>CopyResource</b> can copy between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.
          </li>
<li>Can't be currently mapped.</li>
</ul>
<b>CopyResource</b> only supports copy; it doesn't support any stretch, color key, or blend. To reinterpret the resource data between a few format types (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>) use <b>CopyTextureRegion</b> instead.
        

You can use a   <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">depth-stencil</a> resource as either a source or a destination. Resources created with multi-sampling capability (see <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a>) can be used as source and destination only if both source and destination have identical multi-sampled count and quality. If source and destination differ in multi-sampled count and quality or if one is multi-sampled and the other is not multi-sampled, the call to <b>CopyResource</b> fails. Use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource">ResolveSubresource</a> to resolve a multi-sampled resource to a resource that is not multi-sampled.
        

The method is an asynchronous call, which may be added to the command-buffer queue. This attempts to remove pipeline stalls that may occur when copying data. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">performance considerations</a>.
        

Consider using <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">CopyTextureRegion</a> or <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion">CopyBufferRegion</a> if you only need to copy a portion of the data in a resource.
        


#### Examples

The <a href="/windows/desktop/direct3d12/working-samples">D3D12HeterogeneousMultiadapter</a> sample uses <b>CopyResource</b> in the following way: 

<pre class="syntax" xml:space="preserve"><code>	// Command list to copy the render target to the shared heap on the primary adapter. 
 	{ 
 		const GraphicsAdapter adapter = Primary; 
 
 
 		// Reset the copy command allocator and command list. 
 		ThrowIfFailed(m_copyCommandAllocators[m_frameIndex]-&gt;Reset()); 
 		ThrowIfFailed(m_copyCommandList-&gt;Reset(m_copyCommandAllocators[m_frameIndex].Get(), nullptr)); 
 
 
 		// Copy the intermediate render target to the cross-adapter shared resource. 
 		// Transition barriers are not required since there are fences guarding against 
 		// concurrent read/write access to the shared heap. 
 		if (m_crossAdapterTextureSupport) 
 		{ 
 			// If cross-adapter row-major textures are supported by the adapter, 
 			// simply copy the texture into the cross-adapter texture. 
 			m_copyCommandList-&gt;CopyResource(m_crossAdapterResources[adapter][m_frameIndex].Get(), m_renderTargets[adapter][m_frameIndex].Get()); 
 		} 
 		else 
 		{ 
 			// If cross-adapter row-major textures are not supported by the adapter, 
 			// the texture will be copied over as a buffer so that the texture row 
 			// pitch can be explicitly managed. 
 
 
 			// Copy the intermediate render target into the shared buffer using the 
 			// memory layout prescribed by the render target. 
 			D3D12_RESOURCE_DESC renderTargetDesc = m_renderTargets[adapter][m_frameIndex]-&gt;GetDesc(); 
 			D3D12_PLACED_SUBRESOURCE_FOOTPRINT renderTargetLayout; 
 
 
 			m_devices[adapter]-&gt;GetCopyableFootprints(&amp;renderTargetDesc, 0, 1, 0, &amp;renderTargetLayout, nullptr, nullptr, nullptr); 
 
 
 			CD3DX12_TEXTURE_COPY_LOCATION dest(m_crossAdapterResources[adapter][m_frameIndex].Get(), renderTargetLayout); 
 			CD3DX12_TEXTURE_COPY_LOCATION src(m_renderTargets[adapter][m_frameIndex].Get(), 0); 
 			CD3DX12_BOX box(0, 0, m_width, m_height); 
 
 
 			m_copyCommandList-&gt;CopyTextureRegion(&amp;dest, 0, 0, 0, &amp;src, &amp;box); 
		} 

 
		ThrowIfFailed(m_copyCommandList-&gt;Close()); 
	} 
</code></pre>

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>
