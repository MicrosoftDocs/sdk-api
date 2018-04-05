---
UID: NF:d3d12.ID3D12GraphicsCommandList.ResolveSubresource
title: ID3D12GraphicsCommandList::ResolveSubresource method
author: windows-driver-content
description: Copy a multi-sampled resource into a non-multi-sampled resource.
old-location: direct3d12\id3d12graphicscommandlist_resolvesubresource.htm
old-project: direct3d12
ms.assetid: F1D4BAD1-B08E-47D0-9D2B-41873D6B4456
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D12GraphicsCommandList, ID3D12GraphicsCommandList interface, ResolveSubresource method, ID3D12GraphicsCommandList::ResolveSubresource, ResolveSubresource method, ResolveSubresource method, ID3D12GraphicsCommandList interface, ResolveSubresource,ID3D12GraphicsCommandList.ResolveSubresource, d3d12/ID3D12GraphicsCommandList::ResolveSubresource, direct3d12.id3d12graphicscommandlist_resolvesubresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12GraphicsCommandList.ResolveSubresource
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12GraphicsCommandList::ResolveSubresource method


## -description


Copy a multi-sampled resource into a non-multi-sampled resource.


## -parameters




### -param pDstResource [in]

Type: <b>ID3D12Resource*</b>


            Destination resource. Must be a created with the <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a> flag and be single-sampled. See
            <a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>.
          


### -param DstSubresource [in]

Type: <b>UINT</b>


            A zero-based index, that identifies the destination subresource. Use <a href="https://msdn.microsoft.com/5C63A315-E21E-498B-A832-6BA2D17FF9A7">D3D12CalcSubresource</a> to calculate the subresource index if the parent resource is complex.
          


### -param pSrcResource [in]

Type: <b>ID3D12Resource*</b>


            Source resource. Must be multisampled.
          


### -param SrcSubresource [in]

Type: <b>UINT</b>


            The source subresource of the source resource.
          


### -param Format [in]

Type: <b>DXGI_FORMAT</b>


            A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> that indicates how the multisampled resource will be resolved to a single-sampled resource.
            See remarks.
          


## -returns




            This method does not return a value.
          




## -remarks



<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>

            The debug layer will issue an error if the subresources referenced by the source view is not in the  <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RESOLVE_SOURCE</a> state.
          


            The debug layer will issue an error if the destination buffer is not in the  <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RESOLVE_DEST</a>state.
          

This API is most useful when re-using the resulting rendertarget of one render pass as an input to a second render pass.

The source and destination resources must be the same resource type and have the same dimensions. In addition, they must have compatible formats. There are three scenarios for this:

<table>
<tr>
<th>Scenario</th>
<th>Requirements</th>
</tr>
<tr>
<td>Source and destination are prestructured and typed</td>
<td>Both the source and destination must have identical formats and that format must be specified in the Format parameter.</td>
</tr>
<tr>
<td>One resource is prestructured and typed and the other is prestructured and typeless</td>
<td>The typed resource must have a format that is compatible with the typeless resource (i.e. the typed resource is DXGI_FORMAT_R32_FLOAT and the typeless resource is DXGI_FORMAT_R32_TYPELESS). The format of the typed resource must be specified in the Format parameter.</td>
</tr>
<tr>
<td>Source and destination are prestructured and typeless</td>
<td>
              Both the source and desintation must have the same typeless format (i.e. both must have DXGI_FORMAT_R32_TYPELESS), and the Format parameter must specify a format that is compatible with the source and destination (i.e. if both are DXGI_FORMAT_R32_TYPELESS then DXGI_FORMAT_R32_FLOAT could be specified in the Format parameter).
              
                For example, given the DXGI_FORMAT_R16G16B16A16_TYPELESS format:
              

<ul>
<li>The source (or dest) format could be DXGI_FORMAT_R16G16B16A16_UNORM</li>
<li>The dest (or source) format could be DXGI_FORMAT_R16G16B16A16_FLOAT</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>



<a href="https://msdn.microsoft.com/C4F92F8A-DBF0-412B-8707-CC4C1BF2D88F">Subresources</a>
 

 

