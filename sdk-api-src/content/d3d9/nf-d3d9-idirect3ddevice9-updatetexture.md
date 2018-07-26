---
UID: NF:d3d9.IDirect3DDevice9.UpdateTexture
title: IDirect3DDevice9::UpdateTexture
author: windows-sdk-content
description: Updates the dirty portions of a texture.
old-location: direct3d9\idirect3ddevice9__updatetexture.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__updatetexture.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 29cd384a-27b9-87ac-3d77-7fb734d0afbe, IDirect3DDevice9 interface [Direct3D 9],UpdateTexture method, IDirect3DDevice9.UpdateTexture, IDirect3DDevice9::UpdateTexture, UpdateTexture, UpdateTexture method [Direct3D 9], UpdateTexture method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::UpdateTexture, direct3d9.idirect3ddevice9__updatetexture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.UpdateTexture
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::UpdateTexture


## -description


Updates the dirty portions of a texture.


## -parameters




### -param pSourceTexture [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface, representing the source texture. The source texture must be in system memory (D3DPOOL_SYSTEMMEM). 


### -param pDestinationTexture [in]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/library/Bb174322(v=VS.85).aspx">IDirect3DBaseTexture9</a> interface, representing the destination texture. The destination texture must be in the D3DPOOL_DEFAULT memory pool. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



You can dirty a portion of a texture by locking it, or by calling one of the following methods. 

<ul>
<li>
<a href="https://msdn.microsoft.com/library/Bb174330(v=VS.85).aspx">IDirect3DCubeTexture9::AddDirtyRect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb205910(v=VS.85).aspx">IDirect3DTexture9::AddDirtyRect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb205942(v=VS.85).aspx">IDirect3DVolumeTexture9::AddDirtyBox</a>
</li>
<li>
<a href="https://msdn.microsoft.com/library/Bb205857(v=VS.85).aspx">IDirect3DDevice9::UpdateSurface</a>
</li>
</ul>
<b>IDirect3DDevice9::UpdateTexture</b> retrieves the dirty portions of the texture by calculating what has been accumulated since the last update operation.

For performance reasons, dirty regions are only recorded for level zero of a texture. For sublevels, it is assumed that the corresponding (scaled) rectangle or box is also dirty. Dirty regions are automatically recorded when LockRect or <a href="https://msdn.microsoft.com/library/Bb205945(v=VS.85).aspx">IDirect3DVolumeTexture9::LockBox</a> is called without D3DLOCK_NO_DIRTY_UPDATE or D3DLOCK_READONLY. Also, the destination surface of <a href="https://msdn.microsoft.com/library/Bb205857(v=VS.85).aspx">IDirect3DDevice9::UpdateSurface</a> is marked dirty.

This method fails if the textures are of different types, if their bottom-level buffers are of different sizes, or if their matching levels do not match. For example, consider a six-level source texture with the following dimensions.
    
    
    



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
32x16, 16x8, 8x4, 4x2, 2x1, 1x1
</pre>
</td>
</tr>
</table></span></div>
This six-level source texture could be the source for the following one-level destination.



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
1x1
</pre>
</td>
</tr>
</table></span></div>
For the following two-level destination.



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
2x1, 1x1
</pre>
</td>
</tr>
</table></span></div>
Or, for the following three-level destination.



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
4x2, 2x1, 1x1
</pre>
</td>
</tr>
</table></span></div>
In addition, this method will fail if the textures are of different formats. If the destination texture has fewer levels than the source, only the matching levels are copied. If the source texture has fewer levels than the destination, the method will fail. 

If the source texture has dirty regions, the copy can be optimized by restricting the copy to only those regions. It is not guaranteed that only those bytes marked dirty will be copied.

Here are the possibilities for source and destination surface combinations:

<ul>
<li>If pSourceTexture is a non-autogenerated mipmap and pDestinationTexture is an autogenerated mipmap, only the topmost matching level is updated, and the destination sublevels are regenerated. All other source sublevels are ignored.</li>
<li>If both pSourceTexture and pDestinationTexture are autogenerated mipmaps, only the topmost matching level is updated. The sublevels from the source are ignored and the destination sublevels are regenerated.</li>
<li>If pSourceTexture is an autogenerated mipmap and pDestinationTexture a non-autogenerated mipmap, UpdateTexture will fail.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb174313(v=VS.85).aspx">IDirect3D9::CreateDevice</a>



<a href="https://msdn.microsoft.com/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>
 

 

