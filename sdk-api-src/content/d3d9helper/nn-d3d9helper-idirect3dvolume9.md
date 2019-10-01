---
UID: NN:d3d9helper.IDirect3DVolume9
title: IDirect3DVolume9 (d3d9helper.h)
author: windows-sdk-content
description: Applications use the methods of the IDirect3DVolume9 interface to manipulate volume resources.
old-location: direct3d9\idirect3dvolume9.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 3502e743-9dc5-6b50-07d2-5a1e110c1543, IDirect3DVolume9, IDirect3DVolume9 interface [Direct3D 9], IDirect3DVolume9 interface [Direct3D 9],described, d3d9helper/IDirect3DVolume9, direct3d9.idirect3dvolume9
ms.topic: interface
f1_keywords: 
 - "d3d9helper/IDirect3DVolume9"
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
 - IDirect3DVolume9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVolume9 interface


## -description


Applications use the methods of the <b>IDirect3DVolume9</b> interface to manipulate volume resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirect3DVolume9</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirect3DVolume9</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-freeprivatedata">FreePrivateData</a>
</td>
<td align="left" width="63%">
Frees the specified private data associated with this volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getcontainer">GetContainer</a>
</td>
<td align="left" width="63%">
Provides access to the parent volume texture object, if this surface is a child level of a volume texture.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getdevice">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves the device associated with a volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-getprivatedata">GetPrivateData</a>
</td>
<td align="left" width="63%">
Copies the private data associated with the volume to a provided buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox">LockBox</a>
</td>
<td align="left" width="63%">
Locks a box on a volume resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-setprivatedata">SetPrivateData</a>
</td>
<td align="left" width="63%">
Associates data with the volume that is intended for use by the application, not by Direct3D.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-unlockbox">UnlockBox</a>
</td>
<td align="left" width="63%">
Unlocks a box on a volume resource.

</td>
</tr>
</table> 


## -remarks



The <b>IDirect3DVolume9</b> interface is obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-getvolumelevel">IDirect3DVolumeTexture9::GetVolumeLevel</a> method.

This interface, like all COM interfaces, inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

The LPDIRECT3DVOLUME9 and PDIRECT3DVOLUME9 types are defined as pointers to the <b>IDirect3DVolume9</b> interface.
    

    


```

typedef struct IDirect3DVolume9 *LPDIRECT3DVOLUME9, *PDIRECT3DVOLUME9;

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>
 

 

