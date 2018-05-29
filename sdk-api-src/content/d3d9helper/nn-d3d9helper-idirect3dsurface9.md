---
UID: NN:d3d9helper.IDirect3DSurface9
title: IDirect3DSurface9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DSurface9 interface to query and prepare surfaces.
old-location: direct3d9\idirect3dsurface9.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 7eb0f571-de02-55a6-f6eb-fc92e63fbb48, IDirect3DSurface9, IDirect3DSurface9 interface [Direct3D 9], IDirect3DSurface9 interface [Direct3D 9],described, d3d9helper/IDirect3DSurface9, direct3d9.idirect3dsurface9
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
req.typenames: D3DVSHADERCAPS2_0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d9.lib
-	d3d9.dll
api_name:
-	IDirect3DSurface9
product: Windows
targetos: Windows
req.lib: D3d9.lib
req.dll: 
req.irql: 
---

# IDirect3DSurface9 interface


## -description


Applications use the methods of the IDirect3DSurface9 interface to query and prepare surfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DSurface9</b> interface inherits from <a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>. <b>IDirect3DSurface9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DSurface9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f95f6104-4195-4d01-92c2-512879c9b449">GetContainer</a>
</td>
<td align="left" width="63%">
Provides access to the parent cube texture or texture (mipmap) object, if this surface is a child level of a cube texture or a mipmap. This method can also provide access to the parent swap chain if the surface is a back-buffer child.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3456470b-60c5-4ac2-bb71-714b72e2ed3b">GetDC</a>
</td>
<td align="left" width="63%">
Retrieves a device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3fd1d5c-fb82-4f0d-a8af-ea181456079c">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01f5a1a1-e18f-42c9-9654-34e482f48df8">LockRect</a>
</td>
<td align="left" width="63%">
Locks a rectangle on a surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90a21163-65c2-4409-a18f-5c9a377e9d66">ReleaseDC</a>
</td>
<td align="left" width="63%">
Release a device context handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dc45972-fc17-4a60-9e4a-1d28a379e08f">UnlockRect</a>
</td>
<td align="left" width="63%">
Unlocks a rectangle on a surface.

</td>
</tr>
</table> 


## -remarks



The LPDIRECT3DSURFACE9 and PDIRECT3DSURFACE9 types are defined as pointers to the <b>IDirect3DSurface9</b> interface.
    

    

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirect3DSurface9 *LPDIRECT3DSURFACE9, *PDIRECT3DSURFACE9;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>



<a href="https://msdn.microsoft.com/1fdb0bfe-6e36-49ca-b119-a2b3266037d2">IDirect3DResource9</a>
 

 

