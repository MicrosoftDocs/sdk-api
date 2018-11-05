---
UID: NN:d3d9.IDirect3DVolume9
title: IDirect3DVolume9
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVolume9 interface to manipulate volume resources.
old-location: direct3d9\idirect3dvolume9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 3502e743-9dc5-6b50-07d2-5a1e110c1543, IDirect3DVolume9, IDirect3DVolume9 interface [Direct3D 9], IDirect3DVolume9 interface [Direct3D 9],described, d3d9helper/IDirect3DVolume9, direct3d9.idirect3dvolume9
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
 - IDirect3DVolume9
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DVolume9 interface


## -description


Applications use the methods of the <b>IDirect3DVolume9</b> interface to manipulate volume resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVolume9</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirect3DVolume9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirect3DVolume9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205933(v=VS.85).aspx">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data associated with this volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205934(v=VS.85).aspx">GetContainer</a>
</td>
<td align="left" width="63%">
Provides access to the parent volume texture object, if this surface is a child level of a volume texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205935(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205936(v=VS.85).aspx">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205937(v=VS.85).aspx">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data associated with the volume to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205938(v=VS.85).aspx">LockBox</a>
</td>
<td align="left" width="63%">
Locks a box on a volume resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205939(v=VS.85).aspx">SetPrivateData</a>
</td>
<td align="left" width="63%">
Associates data with the volume that is intended for use by the application, not by Direct3D.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb205940(v=VS.85).aspx">UnlockBox</a>
</td>
<td align="left" width="63%">
Unlocks a box on a volume resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVolume9</b> interface is obtained by calling the <a href="https://msdn.microsoft.com/en-us/library/Bb205944(v=VS.85).aspx">IDirect3DVolumeTexture9::GetVolumeLevel</a> method.

This interface, like all COM interfaces, inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface.

The LPDIRECT3DVOLUME9 and PDIRECT3DVOLUME9 types are defined as pointers to the <b>IDirect3DVolume9</b> interface.
    

    


```

typedef struct IDirect3DVolume9 *LPDIRECT3DVOLUME9, *PDIRECT3DVOLUME9;

```





## -see-also




<a href="https://msdn.microsoft.com/f12facdc-5a3f-4f89-8ae3-a322ef3389b2">Direct3D Interfaces</a>
 

 

