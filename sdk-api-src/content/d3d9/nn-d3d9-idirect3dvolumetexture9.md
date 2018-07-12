---
UID: NN:d3d9.IDirect3DVolumeTexture9
title: IDirect3DVolumeTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.
old-location: direct3d9\idirect3dvolumetexture9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolumetexture9.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IDirect3DVolumeTexture9, IDirect3DVolumeTexture9 interface [Direct3D 9], IDirect3DVolumeTexture9 interface [Direct3D 9],described, ac7e332f-4255-e077-7804-d9a2e2476d37, d3d9helper/IDirect3DVolumeTexture9, direct3d9.idirect3dvolumetexture9
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
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
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DVolumeTexture9 interface


## -description


Applications use the methods of the IDirect3DVolumeTexture9 interface to manipulate a volume texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVolumeTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>. <b>IDirect3DVolumeTexture9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/Bb205942(v=VS.85).aspx">AddDirtyBox</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205943(v=VS.85).aspx">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a level description of a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205944(v=VS.85).aspx">GetVolumeLevel</a>
</td>
<td align="left" width="63%">
Retrieves the specified volume texture level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205945(v=VS.85).aspx">LockBox</a>
</td>
<td align="left" width="63%">
Locks a box on a volume texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb205946(v=VS.85).aspx">UnlockBox</a>
</td>
<td align="left" width="63%">
Unlocks a box on a volume texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVolumeTexture9</b> interface can be obtained by calling the <a href="https://msdn.microsoft.com/library/Bb174367(v=VS.85).aspx">CreateVolumeTexture</a> method or one of the D3DXCreateVolumeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface.

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




<a href="https://msdn.microsoft.com/library/Bb174367(v=VS.85).aspx">CreateVolumeTexture</a>



<a href="https://msdn.microsoft.com/library/Bb172810(v=VS.85).aspx">D3DXCreateVolumeTexture</a>



<a href="https://msdn.microsoft.com/library/Bb172811(v=VS.85).aspx">D3DXCreateVolumeTextureFromFile</a>



<a href="https://msdn.microsoft.com/library/Bb172812(v=VS.85).aspx">D3DXCreateVolumeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/library/Bb172813(v=VS.85).aspx">D3DXCreateVolumeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/library/Bb172814(v=VS.85).aspx">D3DXCreateVolumeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/library/Bb172815(v=VS.85).aspx">D3DXCreateVolumeTextureFromResource</a>



<a href="https://msdn.microsoft.com/library/Bb172816(v=VS.85).aspx">D3DXCreateVolumeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>
 

 

