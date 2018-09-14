---
UID: NN:d3d9.IDirect3DTexture9
title: IDirect3DTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DTexture9 interface to manipulate a texture resource.
old-location: direct3d9\idirect3dtexture9.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDirect3DTexture9, IDirect3DTexture9 interface [Direct3D 9], IDirect3DTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DTexture9, direct3d9.idirect3dtexture9, f2bb39fa-d156-a3ea-9ea0-656a78998f7a
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
 - IDirect3DTexture9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DTexture9 interface


## -description


Applications use the methods of the IDirect3DTexture9 interface to manipulate a texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>. <b>IDirect3DTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71b091d7-d49f-40e8-9068-d97c6ce960b8">AddDirtyRect</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df5758fe-afb8-4821-92f1-53b8022b0e8e">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a level description of a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c64ffb22-dfbd-4da0-aa1c-981f183fe087">GetSurfaceLevel</a>
</td>
<td align="left" width="63%">
Retrieves the specified texture surface level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1c3905a-a253-4e3d-b0b2-99c839a5e6d9">LockRect</a>
</td>
<td align="left" width="63%">
Locks a rectangle on a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/728ead50-5d2e-45a7-a91d-e2d520171d1d">UnlockRect</a>
</td>
<td align="left" width="63%">
Unlocks a rectangle on a texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DTexture9</b> interface can be obtained by calling the <a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">IDirect3DDevice9::CreateTexture</a> method or one of the D3DXCreateTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DTEXTURE9 and PDIRECT3DTEXTURE9 types are defined as pointers to the <b>IDirect3DTexture9</b> interface.
    

    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DTexture9 *LPDIRECT3DTEXTURE9, *PDIRECT3DTEXTURE9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ea028aa9-4f37-4625-9e07-9072ec1a61d0">D3DXCreateTexture</a>



<a href="https://msdn.microsoft.com/247b0ee2-ee31-4090-b94c-41951b46675f">D3DXCreateTextureFromFile</a>



<a href="https://msdn.microsoft.com/820bbd77-98af-4051-a22e-825fa4dd87d8">D3DXCreateTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/3ea811be-7db8-4436-b138-f0102389bb4d">D3DXCreateTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/e515697c-0e24-4d96-b58a-dc4f27683021">D3DXCreateTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/7c841f21-5565-4923-a2fe-bbd618616f87">D3DXCreateTextureFromResource</a>



<a href="https://msdn.microsoft.com/6015e2fa-9deb-4e6a-a401-f10fb05f40b7">D3DXCreateTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/61b27c7f-cfec-4cb1-bdb9-a973c37a7df4">IDirect3DDevice9::CreateTexture</a>
 

 

