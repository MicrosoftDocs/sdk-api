---
UID: NN:d3d9.IDirect3DVolumeTexture9
title: IDirect3DVolumeTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.
old-location: direct3d9\idirect3dvolumetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDirect3DVolumeTexture9, IDirect3DVolumeTexture9 interface [Direct3D 9], IDirect3DVolumeTexture9 interface [Direct3D 9],described, ac7e332f-4255-e077-7804-d9a2e2476d37, d3d9helper/IDirect3DVolumeTexture9, direct3d9.idirect3dvolumetexture9
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDirect3DVolumeTexture9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DVolumeTexture9 interface


## -description


Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVolumeTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>. <b>IDirect3DVolumeTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DVolumeTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f09d099f-d1c1-48c6-a709-f8da2e3e8db1">AddDirtyBox</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d8db22a-6903-4693-a991-2b8dde32bc35">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a level description of a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4df1245-d709-4bbb-863b-6f8c112b49ac">GetVolumeLevel</a>
</td>
<td align="left" width="63%">
Retrieves the specified volume texture level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/732f7711-a71b-4470-824e-4ea0b47e64f7">LockBox</a>
</td>
<td align="left" width="63%">
Locks a box on a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41949c6f-47e7-4f11-9b9c-7b7e56fcc98b">UnlockBox</a>
</td>
<td align="left" width="63%">
Unlocks a box on a volume texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVolumeTexture9</b> interface can be obtained by calling the <a href="https://msdn.microsoft.com/a0dada01-aca1-46ef-8321-62022219843f">CreateVolumeTexture</a> method or one of the D3DXCreateVolumeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DVOLUMETEXTURE9 and PDIRECT3DVOLUMETEXTURE9 types are defined as pointers to the <b>IDirect3DVolumeTexture9</b> interface.
    

    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DVolumeTexture9 *LPDIRECT3DVOLUMETEXTURE9, *PDIRECT3DVOLUMETEXTURE9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a0dada01-aca1-46ef-8321-62022219843f">CreateVolumeTexture</a>



<a href="https://msdn.microsoft.com/8fc515cd-2fb3-40c7-8192-a41d93ac1e99">D3DXCreateVolumeTexture</a>



<a href="https://msdn.microsoft.com/e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d">D3DXCreateVolumeTextureFromFile</a>



<a href="https://msdn.microsoft.com/fa11706a-83cc-4795-957d-6d0e1faf2a8f">D3DXCreateVolumeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/8ea22209-6110-4bef-a0d6-667f59017adc">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/1a43f906-1826-40a3-a7a9-a0536c977164">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/82a0b7aa-69fa-450d-b0d2-769f05fd75ea">D3DXCreateVolumeTextureFromResource</a>



<a href="https://msdn.microsoft.com/02f2cb9e-4750-4854-aa74-202426427af5">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>
 

 

