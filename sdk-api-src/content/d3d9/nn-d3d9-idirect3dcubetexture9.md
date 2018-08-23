---
UID: NN:d3d9.IDirect3DCubeTexture9
title: IDirect3DCubeTexture9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.
old-location: direct3d9\idirect3dcubetexture9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dcubetexture9.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 44cd2690-0c08-62c5-decf-0c54344edb9b, IDirect3DCubeTexture9, IDirect3DCubeTexture9 interface [Direct3D 9], IDirect3DCubeTexture9 interface [Direct3D 9],described, d3d9helper/IDirect3DCubeTexture9, direct3d9.idirect3dcubetexture9
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d9.h
req.include-header: D3D9.h
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
 - IDirect3DCubeTexture9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DCubeTexture9 interface


## -description


Applications use the methods of the IDirect3DCubeTexture9 interface to manipulate a cube texture resource.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DCubeTexture9</b> interface inherits from <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>. <b>IDirect3DCubeTexture9</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/377536bd-c55c-4ec8-a07c-5addd8e84c3a">AddDirtyRect</a>
</td>
<td align="left" width="63%">
Adds a dirty region to a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ba6ad27-b8e8-400d-a3af-e69cdf53087a">GetCubeMapSurface</a>
</td>
<td align="left" width="63%">
Retrieves a cube texture map surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b3efd79-cd69-4eea-af3a-4aa4d3f79e97">GetLevelDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of one face of the specified cube texture level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/724317a3-1fc7-499d-94b7-759731337a00">LockRect</a>
</td>
<td align="left" width="63%">
Locks a rectangle on a cube texture resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e444bdc-c555-465d-84a8-96aef32d3e77">UnlockRect</a>
</td>
<td align="left" width="63%">
Unlocks a rectangle on a cube texture resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DCubeTexture9</b> interface can be obtained by calling the <a href="https://msdn.microsoft.com/d8ae94bb-5b16-4d08-aeb9-cb15029725c9">IDirect3DDevice9::CreateCubeTexture</a> method or one of the D3DXCreateCubeTexture<i>xxx</i> functions.

This interface inherits additional functionality from the <a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a> interface.

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




<a href="https://msdn.microsoft.com/96cf3fc1-9efc-4b97-a082-2956386145c7">D3DXCreateCubeTexture</a>



<a href="https://msdn.microsoft.com/7ff3b051-568c-4c77-b8a6-b626ba156eb1">D3DXCreateCubeTextureFromFile</a>



<a href="https://msdn.microsoft.com/77e64b33-9282-42fa-978c-a93fa9ba11fc">D3DXCreateCubeTextureFromFileEx</a>



<a href="https://msdn.microsoft.com/f7e99d5a-5479-4f0b-b040-bb07e7e37666">D3DXCreateCubeTextureFromFileInMemory</a>



<a href="https://msdn.microsoft.com/598016eb-9ea9-4dca-a297-5708a957da6a">D3DXCreateCubeTextureFromFileInMemoryEx</a>



<a href="https://msdn.microsoft.com/9153944a-af8b-4365-9e91-fc1136a84caa">D3DXCreateCubeTextureFromResource</a>



<a href="https://msdn.microsoft.com/4d263386-8270-4967-8ef5-e9ac69e502a5">D3DXCreateCubeTextureFromResourceEx</a>



<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/d4d7f8b9-2e7b-4445-8380-2d321a46e064">IDirect3DBaseTexture9</a>



<a href="https://msdn.microsoft.com/d8ae94bb-5b16-4d08-aeb9-cb15029725c9">IDirect3DDevice9::CreateCubeTexture</a>
 

 

