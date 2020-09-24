---
UID: NF:d3d11.ID3D11Device.OpenSharedResource
title: ID3D11Device::OpenSharedResource (d3d11.h)
description: Give a device access to a shared resource created on a different device.
helpviewer_keywords: ["ID3D11Device interface [Direct3D 11]","OpenSharedResource method","ID3D11Device.OpenSharedResource","ID3D11Device::OpenSharedResource","OpenSharedResource","OpenSharedResource method [Direct3D 11]","OpenSharedResource method [Direct3D 11]","ID3D11Device interface","c200398f-7a1d-967e-b12d-6d180c9526f9","d3d11/ID3D11Device::OpenSharedResource","direct3d11.id3d11device_opensharedresource"]
old-location: direct3d11\id3d11device_opensharedresource.htm
tech.root: direct3d11
ms.assetid: bc054547-e098-457e-8c8a-a41496234a63
ms.date: 12/05/2018
ms.keywords: ID3D11Device interface [Direct3D 11],OpenSharedResource method, ID3D11Device.OpenSharedResource, ID3D11Device::OpenSharedResource, OpenSharedResource, OpenSharedResource method [Direct3D 11], OpenSharedResource method [Direct3D 11],ID3D11Device interface, c200398f-7a1d-967e-b12d-6d180c9526f9, d3d11/ID3D11Device::OpenSharedResource, direct3d11.id3d11device_opensharedresource
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
 - ID3D11Device::OpenSharedResource
 - d3d11/ID3D11Device::OpenSharedResource
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
 - ID3D11Device.OpenSharedResource
---

# ID3D11Device::OpenSharedResource


## -description

Give a device access to a shared resource created on a different device.

## -parameters

### -param hResource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a></b>

A resource handle. See remarks.

### -param ReturnedInterface [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) for the resource interface. See remarks.

### -param ppResource [out, optional]

Type: <b>void**</b>

Address of a pointer to the resource we are gaining access to.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D11Buffer) will get the GUID of the interface to a buffer resource.

The unique handle of the resource is obtained differently depending on the type of device that originally created the resource.

To share a resource between two Direct3D 11 devices the resource must have been created with the 
      <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_SHARED</a> flag, if it was created using the ID3D11Device interface. 
      If it was created using a DXGI device interface, then the resource is always shared.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. 
      For example, __uuidof(ID3D11Buffer) will get the GUID of the interface to a buffer resource.

When sharing a resource between two Direct3D 10/11 devices the unique handle of the resource can be obtained by querying the resource for the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> interface and then calling <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle">GetSharedHandle</a>.


```

IDXGIResource* pOtherResource(NULL);
hr = pOtherDeviceResource->QueryInterface( __uuidof(IDXGIResource), (void**)&pOtherResource );
HANDLE sharedHandle;
pOtherResource->GetSharedHandle(&sharedHandle);
      
```


The only resources that can be shared are 2D non-mipmapped textures.

To share a resource between a Direct3D 9 device and a Direct3D 11 device the texture must have been created using 
      the <i>pSharedHandle</i> argument of <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createtexture">CreateTexture</a>.  
      The shared Direct3D 9 handle is then passed to OpenSharedResource in the <i>hResource</i> argument.

The following code illustrates the method calls involved.


```

sharedHandle = NULL; // must be set to NULL to create, can use a valid handle here to open in D3D9 
pDevice9->CreateTexture(..., pTex2D_9, &sharedHandle); 
... 
pDevice11->OpenSharedResource(sharedHandle, __uuidof(ID3D11Resource), (void**)(&tempResource11)); 
tempResource11->QueryInterface(__uuidof(ID3D11Texture2D), (void**)(&pTex2D_11)); 
tempResource11->Release(); 
// now use pTex2D_11 with pDevice11   
      
```


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
If a shared texture is updated on one device <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush">ID3D11DeviceContext::Flush</a> must be called on that device.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>