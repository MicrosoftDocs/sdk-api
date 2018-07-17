---
UID: NN:dxgi.IDXGIResource
title: IDXGIResource
author: windows-sdk-content
description: An IDXGIResource interface allows resource sharing and identifies the memory that a resource resides in.
old-location: direct3ddxgi\idxgiresource.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 74b46980-220f-d8c0-f488-2656b735bb5d, IDXGIResource, IDXGIResource interface [DXGI], IDXGIResource interface [DXGI],described, direct3ddxgi.idxgiresource, dxgi/IDXGIResource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi.h
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIResource
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIResource interface


## -description



        An <b>IDXGIResource</b> interface allows resource sharing and identifies the memory that a resource resides in.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIResource</b> interface inherits from <a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>. <b>IDXGIResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e2ac0ca-12f2-4d93-b0cc-21f8923727ed">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fa92667-2e37-498b-994b-7c576754b86b">GetSharedHandle</a>
</td>
<td align="left" width="63%">
Gets the handle to a shared resource.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/7fa92667-2e37-498b-994b-7c576754b86b">GetSharedHandle</a> anymore to retrieve the handle to a shared resource. Instead, use <a href="https://msdn.microsoft.com/7A53616A-E7AB-4EB7-9B8F-ED43A70B691C">IDXGIResource1::CreateSharedHandle</a> to get a handle for sharing. To use <b>IDXGIResource1::CreateSharedHandle</b>, you  must create the resource as shared and specify that it uses NT handles (that is, you set the <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag). We also recommend that you create shared resources that use NT handles so you can use <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>, <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>, and so on on those shared resources.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5e44fba-14d9-4c30-b9b8-e3143aabcee4">GetUsage</a>
</td>
<td align="left" width="63%">
Get the expected resource usage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed9417ee-8074-4022-bce9-230fec1c7093">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the priority for evicting the resource from memory.

</td>
</tr>
</table> 


## -remarks




            To find out what type of memory a resource is currently located in, use <a href="https://msdn.microsoft.com/a03af142-657b-459d-abba-fdee72e77db9">IDXGIDevice::QueryResourceResidency</a>. To share resources between processes, use <a href="https://msdn.microsoft.com/581117dc-dd3a-47ac-a080-f23e72a82a6f">ID3D10Device::OpenSharedResource</a>. For information about how to share resources between multiple Windows graphics APIs, including Direct3D 11, Direct2D, Direct3D 10, and Direct3D 9Ex, see <a href="https://msdn.microsoft.com/65abf33e-3d15-42ff-99bd-674f24da773e">Surface Sharing Between Windows Graphics APIs</a>.
          


            You can retrieve the <b>IDXGIResource</b>  interface from any video memory resource that you create from a Direct3D 10 and later function. Any Direct3D object that supports <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a> or <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> also supports <b>IDXGIResource</b>. For example, the Direct3D 2D texture object that you create from <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> supports <b>IDXGIResource</b>. You can call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the 2D texture object (<a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a>) to retrieve the <b>IDXGIResource</b> interface. For example, to retrieve the <b>IDXGIResource</b>  interface from  the 2D texture object, use the following code.
          

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIResource * pDXGIResource;
hr = g_pd3dTexture2D-&gt;QueryInterface(__uuidof(IDXGIResource), (void **)&amp;pDXGIResource);</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>
 

 

