---
UID: NF:d3d10.ID3D10Device.OpenSharedResource
title: ID3D10Device::OpenSharedResource
author: windows-sdk-content
description: Give a device access to a shared resource created on a different Direct3d device.
old-location: direct3d10\id3d10device_opensharedresource.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_opensharedresource.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: ID3D10Device interface [Direct3D 10],OpenSharedResource method, ID3D10Device.OpenSharedResource, ID3D10Device::OpenSharedResource, OpenSharedResource, OpenSharedResource method [Direct3D 10], OpenSharedResource method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OpenSharedResource, direct3d10.id3d10device_opensharedresource, e1b41a59-f80c-625e-e0a5-cc59636f10e1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
req.include-header: 
req.redist: 
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3d10.h
api_name:
 - ID3D10Device.OpenSharedResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Device::OpenSharedResource


## -description


Give a device access to a shared resource created on a different Direct3d device. 


## -parameters




### -param hResource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HANDLE</a></b>

A resource handle. See remarks.


### -param ReturnedInterface [in]

Type: <b>REFIID</b>

The globally unique identifier (GUID) for the resource interface. See remarks.


### -param ppResource [out]

Type: <b>void**</b>

Address of a pointer to the resource we are gaining access to.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



To share a resource between two Direct3D 10 devices the resource must have been created with the 
      <a href="https://msdn.microsoft.com/en-us/library/Bb172412(v=VS.85).aspx">D3D10_RESOURCE_MISC_SHARED</a> flag, if it was created using the ID3D10Device interface. 
      If it was created using the IDXGIDevice interface, then the resource is always shared.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. 
      For example, __uuidof(ID3D10Buffer) will get the GUID of the interface to a buffer resource.

When sharing a resource between two Direct3D 10 devices the unique handle of the resource can be obtained by querying the resource for the <a href="https://msdn.microsoft.com/en-us/library/Bb174560(v=VS.85).aspx">IDXGIResource</a> interface and then calling <a href="https://msdn.microsoft.com/en-us/library/Bb174562(v=VS.85).aspx">GetSharedHandle</a>.


```

IDXGIResource* pOtherResource(NULL);
hr = pOtherDeviceResource->QueryInterface( __uuidof(IDXGIResource), (void**)&pOtherResource );
HANDLE sharedHandle;
pOtherResource->GetSharedHandle(&sharedHandle);
      
```


The only resources that can be shared are 2D non-mipmapped textures.

To share a resource between a Direct3D 9 device and a Direct3D 10 device the texture must have been created using 
      the <i>pSharedHandle</i> argument of <a href="https://msdn.microsoft.com/en-us/library/Bb174363(v=VS.85).aspx">CreateTexture</a>.  
      The shared Direct3D 9 handle is then passed to OpenSharedResource in the <i>hResource</i> argument.

The following code illustrates the method calls involved.


```

sharedHandle = NULL; // must be set to NULL to create, can use a valid handle here to open in D3D9 
pDevice9->CreateTexture(..., pTex2D_9, &sharedHandle); 
... 
pDevice10->OpenSharedResource(sharedHandle, __uuidof(ID3D10Resource), (void**)(&tempResource10)); 
tempResource10->QueryInterface(__uuidof(ID3D10Texture2D), (void**)(&pTex2D_10)); 
tempResource10->Release(); 
// now use pTex2D_10 with pDevice10   
      
```


Textures being shared from D3D9 to D3D10 have the following restrictions.

<ul>
<li>Textures must be 2D</li>
<li>Only 1 mip level is allowed</li>
<li>Texture must have default usage</li>
<li>Texture must be write only</li>
<li>MSAA textures are not allowed</li>
<li>Bind flags must have SHADER_RESOURCE and RENDER_TARGET set</li>
<li>Only R10G10B10A2_UNORM, R16G16B16A16_FLOAT and R8G8B8A8_UNORM formats are allowed</li>
</ul>
If a shared texture is updated on one device <a href="https://msdn.microsoft.com/en-us/library/Bb173568(v=VS.85).aspx">ID3D10Device::Flush</a> must be called on that device.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173528(v=VS.85).aspx">ID3D10Device Interface</a>
 

 

