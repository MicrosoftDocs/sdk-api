---
UID: NN:dxgi1_2.IDXGIResource1
title: IDXGIResource1
author: windows-sdk-content
description: An IDXGIResource1 interface extends the IDXGIResource interface by adding support for creating a subresource surface object and for creating a handle to a shared resource.
old-location: direct3ddxgi\idxgiresource1.htm
old-project: direct3ddxgi
ms.assetid: 0ABA9B8D-BEA4-4455-A312-7CFEDEBBF19A
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IDXGIResource1, IDXGIResource1 interface [DXGI], IDXGIResource1 interface [DXGI],described, direct3ddxgi.idxgiresource1, dxgi1_2/IDXGIResource1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIResource1
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIResource1 interface


## -description



        An <b>IDXGIResource1</b> interface extends the <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> interface by adding support for creating a subresource surface object and for creating a handle to a shared resource.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIResource1</b> interface inherits from <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a>. <b>IDXGIResource1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIResource1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7A53616A-E7AB-4EB7-9B8F-ED43A70B691C">CreateSharedHandle</a>
</td>
<td align="left" width="63%">
Creates a handle to a shared resource. You can then use the returned handle with multiple Direct3D devices.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99730AB1-C5D9-41D6-8001-495FF26E8232">CreateSubresourceSurface</a>
</td>
<td align="left" width="63%">
Creates a subresource surface object.

</td>
</tr>
</table> 


## -remarks




          To determine the type of memory a resource is currently located in, use <a href="https://msdn.microsoft.com/a03af142-657b-459d-abba-fdee72e77db9">IDXGIDevice::QueryResourceResidency</a>. 
          To share resources between processes, use <a href="https://msdn.microsoft.com/4751B49E-01DB-467B-879C-743C8B43DDA5">ID3D11Device1::OpenSharedResource1</a>. 
          For information about how to share resources between multiple Windows graphics APIs, including Direct3D 11, Direct2D, Direct3D 10, and Direct3D 9Ex, see <a href="https://msdn.microsoft.com/65abf33e-3d15-42ff-99bd-674f24da773e">Surface Sharing Between Windows Graphics APIs</a>.
        


          You can retrieve the <b>IDXGIResource1</b> interface from any video memory resource that you create from a Direct3D 10 and later function. Any Direct3D object that supports <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a> or <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> also supports <b>IDXGIResource1</b>. For example, the Direct3D 2D texture object that you create from <a href="https://msdn.microsoft.com/69950ce7-9c8e-4f00-860d-e118e2bbc81a">ID3D11Device::CreateTexture2D</a> supports <b>IDXGIResource1</b>. You can call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the 2D texture object (<a href="https://msdn.microsoft.com/49cd6e21-6cb1-45ea-b83a-3c93f0560915">ID3D11Texture2D</a>) to retrieve the <b>IDXGIResource1</b> interface. For example, to retrieve the <b>IDXGIResource1</b>  interface from  the 2D texture object, use the following code.
        

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IDXGIResource1 * pDXGIResource;
hr = g_pd3dTexture2D-&gt;QueryInterface(__uuidof(IDXGIResource1), (void **)&amp;pDXGIResource);</pre>
</td>
</tr>
</table></span></div>
<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a>
 

 

