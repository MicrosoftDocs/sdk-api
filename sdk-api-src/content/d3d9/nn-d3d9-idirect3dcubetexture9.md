---
UID: NN:d3d9.IDirect3DCubeTexture9
title: IDirect3DCubeTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 44cd2690-0c08-62c5-decf-0c54344edb9b, IDirect3DCubeTexture9, IDirect3DCubeTexture9 interface [Direct3D 9], IDirect3DCubeTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DCubeTexture9, direct3d9.idirect3dcubetexture9
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
 - IDirect3DCubeTexture9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DCubeTexture9 interface


## -description


Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DCubeTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>. <b>IDirect3DCubeTexture9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DCubeTexture9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174330(v=VS.85).aspx">AddDirtyRect</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174331(v=VS.85).aspx">GetCubeMapSurface</a>
</td>
<td align="left" width="63%">
Retrieves a cube texture map surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174332(v=VS.85).aspx">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of one face of the specified cube texture level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174334(v=VS.85).aspx">LockRect</a>
</td>
<td align="left" width="63%">
Locks a rectangle on a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174335(v=VS.85).aspx">UnlockRect</a>
</td>
<td align="left" width="63%">
Unlocks a rectangle on a cube texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DCubeTexture9</b> interface can be obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb174355(v=VS.85).aspx">IDirect3DDevice9::CreateCubeTexture</a> method or one of the D3DXCreateCubeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface.

This interface, like all COM interfaces, inherits additional functionality from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DCUBETEXTURE9 and PDIRECT3DCubeTexture9 types are defined as pointers to the <b>IDirect3DCubeTexture9</b> interface.
    

    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DCubeTexture9 *LPDIRECT3DCUBETEXTURE9, *PDIRECT3DCubeTexture9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb172755(v=VS.85).aspx">D3DXCreateCubeTexture</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172756(v=VS.85).aspx">D3DXCreateCubeTextureFromFile</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172757(v=VS.85).aspx">D3DXCreateCubeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172758(v=VS.85).aspx">D3DXCreateCubeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172759(v=VS.85).aspx">D3DXCreateCubeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172760(v=VS.85).aspx">D3DXCreateCubeTextureFromResource</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb172761(v=VS.85).aspx">D3DXCreateCubeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174355(v=VS.85).aspx">IDirect3DDevice9::CreateCubeTexture</a>
 

 

