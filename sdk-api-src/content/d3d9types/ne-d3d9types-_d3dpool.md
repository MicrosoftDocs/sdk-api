---
UID: NE:d3d9types._D3DPOOL
title: "_D3DPOOL"
author: windows-driver-content
description: Defines the memory class that holds the buffers for a resource.
old-location: direct3d9\D3DPOOL.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dpool.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: 10e369e2-be5f-0d8f-0f83-2aaee98e744e, D3DPOOL, D3DPOOL enumeration [Direct3D 9], D3DPOOL_DEFAULT, D3DPOOL_FORCE_DWORD, D3DPOOL_MANAGED, D3DPOOL_SCRATCH, D3DPOOL_SYSTEMMEM, LPD3DPOOL, LPD3DPOOL enumeration pointer [Direct3D 9], _D3DPOOL, d3d9types/D3DPOOL, d3d9types/D3DPOOL_DEFAULT, d3d9types/D3DPOOL_FORCE_DWORD, d3d9types/D3DPOOL_MANAGED, d3d9types/D3DPOOL_SCRATCH, d3d9types/D3DPOOL_SYSTEMMEM, d3d9types/LPD3DPOOL, direct3d9.D3DPOOL
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d9types.h
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
req.typenames: D3DPOOL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D9Types.h
api_name:
-	D3DPOOL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _D3DPOOL enumeration


## -description


Defines the memory class that holds the buffers for a resource.


## -enum-fields




### -field D3DPOOL_DEFAULT

Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource. This is usually video memory, including both local video memory and AGP memory. The D3DPOOL_DEFAULT pool is separate from D3DPOOL_MANAGED and D3DPOOL_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access. Note that D3DPOOL_DEFAULT never indicates that either D3DPOOL_MANAGED or D3DPOOL_SYSTEMMEM should be chosen as the memory pool type for this resource. Textures placed in the D3DPOOL_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats. To access unlockable textures, you must use functions such as <a href="https://msdn.microsoft.com/303a4224-9c5d-4fc6-a7c5-168f18166e3c">IDirect3DDevice9::UpdateSurface</a>, <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a>, <a href="https://msdn.microsoft.com/7a5e34b4-baec-4305-b0ca-d09b0925a2ef">IDirect3DDevice9::GetFrontBufferData</a>, and <a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">IDirect3DDevice9::GetRenderTargetData</a>. D3DPOOL_MANAGED is probably a better choice than D3DPOOL_DEFAULT for most applications. Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked. Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked. When a device is lost, resources created using D3DPOOL_DEFAULT must be released before calling <a href="https://msdn.microsoft.com/6d672f22-9843-4ff7-ae79-4903f56cd1e9">IDirect3DDevice9::Reset</a>. For more information, see <a href="https://msdn.microsoft.com/dc4326ba-2ebc-4bca-8fba-02d8db739b8f">Lost Devices (Direct3D 9)</a>. 

When creating resources with D3DPOOL_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.


### -field D3DPOOL_MANAGED

Resources are copied automatically to device-accessible memory as needed. Managed resources are backed by system memory and do not need to be recreated when a device is lost. See <a href="https://msdn.microsoft.com/4aa55313-b86c-48e7-829a-a0917c2ebae7">Managing Resources (Direct3D 9)</a> for more information. Managed resources can be locked. Only the system-memory copy is directly modified. Direct3D copies your changes to driver-accessible memory as needed.



<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

D3DPOOL_MANAGED is valid with <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>; however, it is not valid with <a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>.

</td>
</tr>
</table>
 


### -field D3DPOOL_SYSTEMMEM

Resources are placed in memory that is not typically accessible by the Direct3D device. This memory allocation consumes system RAM but does not reduce pageable RAM. These resources do not need to be recreated when a device is lost. Resources in this pool can be locked and can be used as the source for a <a href="https://msdn.microsoft.com/303a4224-9c5d-4fc6-a7c5-168f18166e3c">IDirect3DDevice9::UpdateSurface</a> or <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a> operation to a memory resource created with D3DPOOL_DEFAULT. 


### -field D3DPOOL_SCRATCH

Resources are placed in system RAM and do not need to be recreated when a device is lost.  These resources are not bound by device size or format restrictions.  Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets. However, these resources can always be created, locked, and copied.


### -field D3DPOOL_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -remarks



All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.

The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages. An x indicates a compatible combination; lack of an x indicates incompatibility.

<table>
<tr>
<th>Pool</th>
<th>D3DUSAGE_RENDERTARGET</th>
<th>D3DUSAGE_DEPTHSTENCIL</th>
</tr>
<tr>
<th>D3DPOOL_DEFAULT</th>
<td>x</td>
<td>x</td>
</tr>
<tr>
<th>D3DPOOL_MANAGED</th>
<td></td>
<td></td>
</tr>
<tr>
<th>D3DPOOL_SCRATCH</th>
<td></td>
<td></td>
</tr>
<tr>
<th>D3DPOOL_SYSTEMMEM</th>
<td></td>
<td></td>
</tr>
</table>
 

<table>
<tr>
<th>Pool</th>
<th>D3DUSAGE_DYNAMIC</th>
<th>D3DUSAGE_AUTOGENMIPMAP</th>
</tr>
<tr>
<th>D3DPOOL_DEFAULT</th>
<td>x</td>
<td>x</td>
</tr>
<tr>
<th>D3DPOOL_MANAGED</th>
<td></td>
<td>x</td>
</tr>
<tr>
<th>D3DPOOL_SCRATCH</th>
<td></td>
<td></td>
</tr>
<tr>
<th>D3DPOOL_SYSTEMMEM</th>
<td>x</td>
<td></td>
</tr>
</table>
 

For more information about usage types, see <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>.

Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.

Applications should use D3DPOOL_MANAGED for most static resources because this saves the application from having to deal with lost devices. (Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems. Other dynamic resources are not a good match for D3DPOOL_MANAGED. In fact, index buffers and vertex buffers cannot be created using D3DPOOL_MANAGED together with D3DUSAGE_DYNAMIC.

For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL_DEFAULT and the system memory using D3DPOOL_SYSTEMMEM. You can lock and modify the bits of the system memory texture using a locking method. Then you can update the video memory texture using <a href="https://msdn.microsoft.com/79be31d9-0dd2-416c-b58c-9b3b7777c65c">IDirect3DDevice9::UpdateTexture</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d45213e-b3c0-4eb7-a4f9-8d8730eb3899">D3DINDEXBUFFER_DESC</a>



<a href="https://msdn.microsoft.com/fad8ffdb-36e5-4695-b343-e1315357c31a">D3DSURFACE_DESC</a>



<a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a>



<a href="https://msdn.microsoft.com/0ae8f976-d0ca-4d55-b6db-5be85fa3c799">D3DVERTEXBUFFER_DESC</a>



<a href="https://msdn.microsoft.com/c0224f4e-3d32-4bdd-b56c-4e8aa291bb27">D3DVOLUME_DESC</a>



<a href="https://msdn.microsoft.com/ae64eb17-63a8-44c5-8d41-e021c49f338a">Direct3D Enumerations</a>



<a href="https://msdn.microsoft.com/d8ae94bb-5b16-4d08-aeb9-cb15029725c9">IDirect3DDevice9::CreateCubeTexture</a>



<a href="https://msdn.microsoft.com/8bfc9f23-ea7a-411b-82b9-5f19cb2f81e0">IDirect3DDevice9::CreateIndexBuffer</a>



<a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">IDirect3DDevice9::CreateTexture</a>



<a href="https://msdn.microsoft.com/7b914bbd-d4bb-4d59-9820-f494a4cf0757">IDirect3DDevice9::CreateVertexBuffer</a>



<a href="https://msdn.microsoft.com/a0dada01-aca1-46ef-8321-62022219843f">IDirect3DDevice9::CreateVolumeTexture</a>
 

 

