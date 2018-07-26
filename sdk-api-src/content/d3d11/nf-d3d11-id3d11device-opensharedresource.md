---
UID: NF:d3d11.ID3D11Device.OpenSharedResource
title: ID3D11Device::OpenSharedResource
author: windows-sdk-content
description: Give a device access to a shared resource created on a different device.
old-location: direct3d11\id3d11device_opensharedresource.htm
old-project: direct3d11
ms.assetid: bc054547-e098-457e-8c8a-a41496234a63
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: ID3D11Device interface [Direct3D 11],OpenSharedResource method, ID3D11Device.OpenSharedResource, ID3D11Device::OpenSharedResource, OpenSharedResource, OpenSharedResource method [Direct3D 11], OpenSharedResource method [Direct3D 11],ID3D11Device interface, c200398f-7a1d-967e-b12d-6d180c9526f9, d3d11/ID3D11Device::OpenSharedResource, direct3d11.id3d11device_opensharedresource
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
 - ID3D11Device.OpenSharedResource
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::OpenSharedResource


## -description


Give a device access to a shared resource created on a different device.


## -parameters




### -param hResource [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a></b>

A resource handle. See remarks.


### -param ReturnedInterface [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) for the resource interface. See remarks.


### -param ppResource [out, optional]

Type: <b>void**</b>

Address of a pointer to the resource we are gaining access to.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D11Buffer) will get the GUID of the interface to a buffer resource.

The unique handle of the resource is obtained differently depending on the type of device that originally created the resource.

To share a resource between two Direct3D 11 devices the resource must have been created with the 
      <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_SHARED</a> flag, if it was created using the ID3D11Device interface. 
      If it was created using a DXGI device interface, then the resource is always shared.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. 
      For example, __uuidof(ID3D11Buffer) will get the GUID of the interface to a buffer resource.

When sharing a resource between two Direct3D 10/11 devices the unique handle of the resource can be obtained by querying the resource for the <a href="https://msdn.microsoft.com/de1f11a5-194b-438e-975b-3945179d0ed7">IDXGIResource</a> interface and then calling <a href="https://msdn.microsoft.com/7fa92667-2e37-498b-994b-7c576754b86b">GetSharedHandle</a>.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
IDXGIResource* pOtherResource(NULL);
hr = pOtherDeviceResource-&gt;QueryInterface( __uuidof(IDXGIResource), (void**)&amp;pOtherResource );
HANDLE sharedHandle;
pOtherResource-&gt;GetSharedHandle(&amp;sharedHandle);
      </pre>
</td>
</tr>
</table></span></div>
The only resources that can be shared are 2D non-mipmapped textures.

To share a resource between a Direct3D 9 device and a Direct3D 11 device the texture must have been created using 
      the <i>pSharedHandle</i> argument of <a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">CreateTexture</a>.  
      The shared Direct3D 9 handle is then passed to OpenSharedResource in the <i>hResource</i> argument.

The following code illustrates the method calls involved.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
sharedHandle = NULL; // must be set to NULL to create, can use a valid handle here to open in D3D9 
pDevice9-&gt;CreateTexture(..., pTex2D_9, &amp;sharedHandle); 
... 
pDevice11-&gt;OpenSharedResource(sharedHandle, __uuidof(ID3D11Resource), (void**)(&amp;tempResource11)); 
tempResource11-&gt;QueryInterface(__uuidof(ID3D11Texture2D), (void**)(&amp;pTex2D_11)); 
tempResource11-&gt;Release(); 
// now use pTex2D_11 with pDevice11   
      </pre>
</td>
</tr>
</table></span></div>
Textures being shared from D3D9 to D3D11 have the following restrictions.

<ul>
<li>Textures must be 2D</li>
<li>Only 1 mip level is allowed</li>
<li>Texture must have default usage</li>
<li>Texture must be write only</li>
<li>MSAA textures are not allowed</li>
<li>Bind flags must have SHADER_RESOURCE and RENDER_TARGET set</li>
<li>Only R10G10B10A2_UNORM, R16G16B16A16_FLOAT and R8G8B8A8_UNORM formats are allowed</li>
</ul>
If a shared texture is updated on one device <a href="https://msdn.microsoft.com/e204c585-4996-4274-a654-b9912e957fe6">ID3D11DeviceContext::Flush</a> must be called on that device.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

