---
UID: NE:d3d10.D3D10_RESOURCE_MISC_FLAG
title: D3D10_RESOURCE_MISC_FLAG
author: windows-sdk-content
description: Identifies other, less common options for resources.
old-location: direct3d10\d3d10_resource_misc_flag.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_resource_misc_flag.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 933479cf-687a-018f-fa4e-e44396ff5c4b, D3D10_RESOURCE_MISC_FLAG, D3D10_RESOURCE_MISC_FLAG enumeration [Direct3D 10], D3D10_RESOURCE_MISC_GDI_COMPATIBLE, D3D10_RESOURCE_MISC_GENERATE_MIPS, D3D10_RESOURCE_MISC_SHARED, D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX, D3D10_RESOURCE_MISC_TEXTURECUBE, d3d10/D3D10_RESOURCE_MISC_FLAG, d3d10/D3D10_RESOURCE_MISC_GDI_COMPATIBLE, d3d10/D3D10_RESOURCE_MISC_GENERATE_MIPS, d3d10/D3D10_RESOURCE_MISC_SHARED, d3d10/D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX, d3d10/D3D10_RESOURCE_MISC_TEXTURECUBE, direct3d10.d3d10_resource_misc_flag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_RESOURCE_MISC_FLAG
product: Windows
targetos: Windows
req.typenames: D3D10_RESOURCE_MISC_FLAG
req.redist: 
---

# D3D10_RESOURCE_MISC_FLAG enumeration


## -description


Identifies other, less common options for resources.


## -enum-fields




### -field D3D10_RESOURCE_MISC_GENERATE_MIPS

Enables an application to call <a href="https://msdn.microsoft.com/bc3491b6-99fb-4560-bce1-dd7758626cf9">ID3D10Device::GenerateMips</a> on 
        a <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">texture resource</a>. The resource must be created 
        with the <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">bind flags</a> that specify that the resource is a render target and a shader resource.


### -field D3D10_RESOURCE_MISC_SHARED

Enables the sharing of resource data between two or more Direct3D devices. The only resources that can be shared are 2D non-mipmapped textures.

WARP and REF devices do not support shared resources. Attempting to create a resource with this flag on either a WARP or REF device will cause the
        create method to return an E_OUTOFMEMORY error code.


### -field D3D10_RESOURCE_MISC_TEXTURECUBE

Enables an application to create a cube texture from a 
        <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Texture2DArray</a> that contains 6 textures.


### -field D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX

Enables the resource created to be synchronized using the IDXGIKeyedMutex::AcquireSync and ReleaseSync APIs. 
            The following resource creation D3D10 APIs, that all take a D3D10_RESOURCE_MISC_FLAG parameter, have been extended to support the new flag.

<ul>
<li>ID3D10Device1::CreateTexture1D</li>
<li>ID3D10Device1::CreateTexture2D</li>
<li>ID3D10Device1::CreateTexture3D</li>
<li>ID3D10Device1::CreateBuffer</li>
</ul>
If any of the listed functions are called with the D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX flag set, the interface returned can be 
            queried for an IDXGIKeyedMutex interface, which implements AcquireSync and ReleaseSync APIs to synchronize access to the surface. 
            The device creating the surface, and any other device opening the surface (using OpenSharedResource) is required to 
            call IDXGIKeyedMutex::AcquireSync before any rendering commands to the surface, and IDXGIKeyedMutex::ReleaseSync when it is done rendering.

WARP and REF devices do not support shared resources. Attempting to create a resource with this flag on either a WARP or REF device will cause the
          create method to return an E_OUTOFMEMORY error code.


### -field D3D10_RESOURCE_MISC_GDI_COMPATIBLE

Enables a surface to be used for GDI interoperability.  Setting this flag enables rendering on the surface 
        via IDXGISurface1::GetDC.


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/3f98c741-ff4c-4080-bd57-ef35cd6622d6">D3D10_BUFFER_DESC</a>, <a href="https://msdn.microsoft.com/f4230e66-5b38-4c69-8406-974fb7708c16">D3D10_TEXTURE1D_DESC</a>, <a href="https://msdn.microsoft.com/2535da35-7985-4e50-b840-6a636f871697">D3D10_TEXTURE2D_DESC</a>, 
      <a href="https://msdn.microsoft.com/b2447872-cbef-4cf2-ab7c-2739343ceb64">D3D10_TEXTURE3D_DESC</a>, <a href="https://msdn.microsoft.com/40d89166-cc11-490d-867c-ae5db23a0784">D3DX10_IMAGE_INFO</a>, and <a href="https://msdn.microsoft.com/8325d50e-a8a9-4ee2-87e2-e60fb3699af6">D3DX10_IMAGE_LOAD_INFO</a>.

These flags can be combined by bitwise OR.

D3D10_RESOURCE_MISC_SHARED and D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX are mutually exclusive flags: 
      either one may be set in the resource creation calls but not both simultaneously.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

