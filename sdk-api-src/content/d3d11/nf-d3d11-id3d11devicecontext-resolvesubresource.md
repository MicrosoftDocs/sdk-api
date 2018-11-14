---
UID: NF:d3d11.ID3D11DeviceContext.ResolveSubresource
title: ID3D11DeviceContext::ResolveSubresource
author: windows-sdk-content
description: Copy a multisampled resource into a non-multisampled resource.
old-location: direct3d11\id3d11devicecontext_resolvesubresource.htm
tech.root: direct3d11
ms.assetid: 7b4d6180-e3bf-475a-9865-592cda6e9f4a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 9790b3fd-189f-fe3d-b1be-96c2ba68f3f3, ID3D11DeviceContext interface [Direct3D 11],ResolveSubresource method, ID3D11DeviceContext.ResolveSubresource, ID3D11DeviceContext::ResolveSubresource, ResolveSubresource, ResolveSubresource method [Direct3D 11], ResolveSubresource method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::ResolveSubresource, direct3d11.id3d11devicecontext_resolvesubresource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.ResolveSubresource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.ResolveSubresource
: 
---

# ID3D11DeviceContext::ResolveSubresource


## -description


Copy a multisampled resource into a non-multisampled resource.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

Destination resource. Must be a created with the <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE_DEFAULT</a> flag and be single-sampled. See <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>.


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based index, that identifies the destination subresource. Use <a href="https://msdn.microsoft.com/643a21f7-3c2e-4d62-9236-051f51d31241">D3D11CalcSubresource</a> to calculate the index.


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

Source resource. Must be multisampled.


### -param SrcSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The source subresource of the source resource.


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> that indicates how the multisampled resource will be resolved to a single-sampled resource. 
      See remarks.


## -returns



Returns nothing.




## -remarks



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
<td>Both the source and desintation must have the same typeless format (i.e. both must have DXGI_FORMAT_R32_TYPELESS), and the Format parameter must specify a format that is compatible with the source and destination (i.e. if both are DXGI_FORMAT_R32_TYPELESS then DXGI_FORMAT_R32_FLOAT could be specified in the Format parameter).

For example, given the DXGI_FORMAT_R16G16B16A16_TYPELESS format:

<ul>
<li>The source (or dest) format could be DXGI_FORMAT_R16G16B16A16_UNORM</li>
<li>The dest (or source) format could be DXGI_FORMAT_R16G16B16A16_FLOAT</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

