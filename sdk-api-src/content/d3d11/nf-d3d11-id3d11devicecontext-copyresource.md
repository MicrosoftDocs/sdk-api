---
UID: NF:d3d11.ID3D11DeviceContext.CopyResource
title: ID3D11DeviceContext::CopyResource
author: windows-sdk-content
description: Copy the entire contents of the source resource to the destination resource using the GPU.
old-location: direct3d11\id3d11devicecontext_copyresource.htm
old-project: direct3d11
ms.assetid: 54c1c08a-792c-463d-8237-9f7947d15396
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CopyResource, CopyResource method [Direct3D 11], CopyResource method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CopyResource method, ID3D11DeviceContext.CopyResource, ID3D11DeviceContext::CopyResource, b389573e-412e-6a72-6e59-396d4bd62341, d3d11/ID3D11DeviceContext::CopyResource, direct3d11.id3d11devicecontext_copyresource
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.CopyResource
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::CopyResource


## -description


Copy the entire contents of the source resource to the destination resource using the GPU. 


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface that represents the destination resource.


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> interface that represents the source resource.


## -returns



Returns nothing




## -remarks



This method is unusual in that it causes the GPU to perform the copy operation (similar to a memcpy by the CPU). As a result, it has a few restrictions designed for improving performance. For instance, the source and destination resources:

<ul>
<li>Must be different resources.</li>
<li>Must be the same type.</li>
<li>Must have identical dimensions (including width, height, depth, and size as appropriate).</li>
<li>Must have compatible <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI formats</a>, which means the formats must be identical or at least from the same type group. For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to an DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. <a href="https://msdn.microsoft.com/en-us/library/Bb173541(v=VS.85).aspx">CopyResource</a> can copy between a few format types. For more info, see <a href="https://msdn.microsoft.com/en-us/library/Bb694531(v=VS.85).aspx">Format Conversion using Direct3D 10.1</a>.</li>
<li>Can't be currently mapped.</li>
</ul>
<b>CopyResource</b> only supports copy; it doesn't support any stretch, color key, or blend. <a href="https://msdn.microsoft.com/en-us/library/Bb173541(v=VS.85).aspx">CopyResource</a> can reinterpret the resource data between a few format types. For more info, see <a href="https://msdn.microsoft.com/en-us/library/Bb694531(v=VS.85).aspx">Format Conversion using Direct3D 10.1</a>.

You can't use an <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">Immutable</a> resource as a destination. You can use a   <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">depth-stencil</a> resource as either a source or a destination provided that the feature level is D3D_FEATURE_LEVEL_10_1 or greater. For feature levels 9_x, resources created with the D3D11_BIND_DEPTH_STENCIL flag can only be used as a source for <a href="https://msdn.microsoft.com/en-us/library/Bb173541(v=VS.85).aspx">CopyResource</a>.  Resources created with multisampling capability (see <a href="https://msdn.microsoft.com/en-us/library/Bb173072(v=VS.85).aspx">DXGI_SAMPLE_DESC</a>) can be used as source and destination only if both source and destination have identical multisampled count and quality. If source and destination differ in multisampled count and quality or if one is multisampled and the other is not multisampled, the call to <b>ID3D11DeviceContext::CopyResource</b> fails. Use <a href="https://msdn.microsoft.com/7b4d6180-e3bf-475a-9865-592cda6e9f4a">ID3D11DeviceContext::ResolveSubresource</a> to resolve a multisampled resource to a resource that is not multisampled.

The method is an asynchronous call, which may be added to the command-buffer queue. This attempts to remove pipeline stalls that may occur when copying data. For more info, see <a href="https://msdn.microsoft.com/en-us/library/Bb205132(v=VS.85).aspx">performance considerations</a>.

We recommend to use <a href="https://msdn.microsoft.com/aed89483-9870-445d-96e3-a9cee764f0ad">ID3D11DeviceContext::CopySubresourceRegion</a> instead if you only need to copy a portion of the data in a resource.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>



<a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>
 

 

