---
UID: NN:d3d9.IDirect3DBaseTexture9
title: IDirect3DBaseTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DBaseTexture9 interface to manipulate texture resources including cube and volume textures.
old-location: direct3d9\idirect3dbasetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dbasetexture9.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: 9a51f87c-558e-0e06-6372-a3753ac70d17, IDirect3DBaseTexture9, IDirect3DBaseTexture9 interface [Direct3D 9], IDirect3DBaseTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DBaseTexture9, direct3d9.idirect3dbasetexture9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d9.lib
 - d3d9.dll
api_name:
 - IDirect3DBaseTexture9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DBaseTexture9 interface


## -description


Applications use the methods of the IDirect3DBaseTexture9 interface to manipulate texture resources including cube and volume textures.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DBaseTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>. <b>IDirect3DBaseTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DBaseTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4fd7fcb3-d3fc-4db9-a56b-d5008e32c0c7">GenerateMipSubLevels</a>
</td>
<td align="left" width="63%">
Generate mipmap sublevels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dd29318-ddf3-4d21-9b6e-fa0e2512a004">GetAutoGenFilterType</a>
</td>
<td align="left" width="63%">
Get the filter type that is used for automatically generated mipmap sublevels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2174bc73-c888-4856-bb4b-ce4b9b6c581d">GetLevelCount</a>
</td>
<td align="left" width="63%">
Returns the number of texture levels in a multilevel texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56f998a3-1f4e-406b-a108-bbc7cc8bdef1">GetLOD</a>
</td>
<td align="left" width="63%">
Returns a value clamped to the maximum level-of-detail set for a managed texture (this method is not supported for an unmanaged texture).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa742bfe-e4b2-48f6-8d84-3772b519aab3">SetAutoGenFilterType</a>
</td>
<td align="left" width="63%">
Set the filter type that is used for automatically generated mipmap sublevels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/724892c1-39c0-44c6-bb94-d09da4fee4ac">SetLOD</a>
</td>
<td align="left" width="63%">
Sets the most detailed level-of-detail for a managed texture. 

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DBaseTexture9</b> interface assigned to a particular stage for a device is obtained by calling the <a href="https://msdn.microsoft.com/f472de6f-6c46-4424-95e5-62164afaf026">GetTexture</a> method.

The LPDIRECT3DBASETEXTURE9 and PDIRECT3DBASETEXTURE9 types are defined as pointers to the <b>IDirect3DBaseTexture9</b> interface.





```
typedef struct IDirect3DBaseTexture9 *LPDIRECT3DBASETEXTURE9, *PDIRECT3DBASETEXTURE9;
```





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>
 

 

