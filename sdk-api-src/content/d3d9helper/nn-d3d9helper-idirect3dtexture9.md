---
UID: NN:d3d9helper.IDirect3DTexture9
title: IDirect3DTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DTexture9 interface to manipulate a texture resource.
old-location: direct3d9\idirect3dtexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dtexture9.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDirect3DTexture9, IDirect3DTexture9 interface [Direct3D 9], IDirect3DTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DTexture9, direct3d9.idirect3dtexture9, f2bb39fa-d156-a3ea-9ea0-656a78998f7a
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9helper.h
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>. <b>IDirect3DTexture9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb205910(v=VS.85).aspx">AddDirtyRect</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205911(v=VS.85).aspx">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a level description of a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205912(v=VS.85).aspx">GetSurfaceLevel</a>
</td>
<td align="left" width="63%">
Retrieves the specified texture surface level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205913(v=VS.85).aspx">LockRect</a>
</td>
<td align="left" width="63%">
Locks a rectangle on a texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205914(v=VS.85).aspx">UnlockRect</a>
</td>
<td align="left" width="63%">
Unlocks a rectangle on a texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DTexture9</b> interface can be obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb174363(v=VS.85).aspx">IDirect3DDevice9::CreateTexture</a> method or one of the D3DXCreateTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DTEXTURE9 and PDIRECT3DTEXTURE9 types are defined as pointers to the <b>IDirect3DTexture9</b> interface.
    

    


```

typedef struct IDirect3DTexture9 *LPDIRECT3DTEXTURE9, *PDIRECT3DTEXTURE9;

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172800(v=VS.85).aspx">D3DXCreateTexture</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172801(v=VS.85).aspx">D3DXCreateTextureFromFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172802(v=VS.85).aspx">D3DXCreateTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172803(v=VS.85).aspx">D3DXCreateTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172804(v=VS.85).aspx">D3DXCreateTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172805(v=VS.85).aspx">D3DXCreateTextureFromResource</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172806(v=VS.85).aspx">D3DXCreateTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174363(v=VS.85).aspx">IDirect3DDevice9::CreateTexture</a>
 

 

