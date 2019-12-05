---
UID: NN:dxgi.IDXGIResource
title: IDXGIResource (dxgi.h)
description: An IDXGIResource interface allows resource sharing and identifies the memory that a resource resides in.
old-location: direct3ddxgi\idxgiresource.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiresource.htm
ms.date: 12/05/2018
ms.keywords: 74b46980-220f-d8c0-f488-2656b735bb5d, IDXGIResource, IDXGIResource interface [DXGI], IDXGIResource interface [DXGI],described, direct3ddxgi.idxgiresource, dxgi/IDXGIResource
ms.topic: interface
f1_keywords:
- dxgi/IDXGIResource
dev_langs:
- c++
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIResource interface


## -description


An <b>IDXGIResource</b> interface allows resource sharing and identifies the memory that a resource resides in.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIResource</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>. <b>IDXGIResource</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getevictionpriority">GetEvictionPriority</a>
</td>
<td align="left" width="63%">
Get the eviction priority.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle">GetSharedHandle</a>
</td>
<td align="left" width="63%">
Gets the handle to a shared resource.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle">GetSharedHandle</a> anymore to retrieve the handle to a shared resource. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle">IDXGIResource1::CreateSharedHandle</a> to get a handle for sharing. To use <b>IDXGIResource1::CreateSharedHandle</b>, you  must create the resource as shared and specify that it uses NT handles (that is, you set the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag). We also recommend that you create shared resources that use NT handles so you can use <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>, <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, and so on on those shared resources.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getusage">GetUsage</a>
</td>
<td align="left" width="63%">
Get the expected resource usage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-setevictionpriority">SetEvictionPriority</a>
</td>
<td align="left" width="63%">
Set the priority for evicting the resource from memory.

</td>
</tr>
</table> 


## -remarks



To find out what type of memory a resource is currently located in, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-queryresourceresidency">IDXGIDevice::QueryResourceResidency</a>. To share resources between processes, use <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10device-opensharedresource">ID3D10Device::OpenSharedResource</a>. For information about how to share resources between multiple Windows graphics APIs, including Direct3D 11, Direct2D, Direct3D 10, and Direct3D 9Ex, see <a href="https://docs.microsoft.com/windows/desktop/direct3darticles/surface-sharing-between-windows-graphics-apis">Surface Sharing Between Windows Graphics APIs</a>.
          

You can retrieve the <b>IDXGIResource</b>  interface from any video memory resource that you create from a Direct3D 10 and later function. Any Direct3D object that supports <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> also supports <b>IDXGIResource</b>. For example, the Direct3D 2D texture object that you create from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture2d">ID3D11Device::CreateTexture2D</a> supports <b>IDXGIResource</b>. You can call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the 2D texture object (<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d">ID3D11Texture2D</a>) to retrieve the <b>IDXGIResource</b> interface. For example, to retrieve the <b>IDXGIResource</b>  interface from  the 2D texture object, use the following code.
          


```
IDXGIResource * pDXGIResource;
hr = g_pd3dTexture2D->QueryInterface(__uuidof(IDXGIResource), (void **)&pDXGIResource);
```


<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>
 

 

