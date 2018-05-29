---
UID: NF:d3d9helper.IDirect3DVolume9.GetContainer
title: IDirect3DVolume9::GetContainer
author: windows-sdk-content
description: Provides access to the parent volume texture object, if this surface is a child level of a volume texture.
old-location: direct3d9\idirect3dvolume9__getcontainer.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getcontainer.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 0941591e-d47b-5e74-736a-768203a929fd, GetContainer, GetContainer method [Direct3D 9], GetContainer method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetContainer method, IDirect3DVolume9.GetContainer, IDirect3DVolume9::GetContainer, d3d9helper/IDirect3DVolume9::GetContainer, direct3d9.idirect3dvolume9__getcontainer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DVolume9.GetContainer
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVolume9::GetContainer


## -description


Provides access to the parent volume texture object, if this surface is a child level of a volume texture.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the volume being requested. 


### -param ppContainer [out, retval]

Type: <b>void**</b>

Address of a pointer to fill with the container pointer, if the query succeeds. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



If the call succeeds, the reference count of the container is increased by one.

Here's an example getting the parent volume texture of a volume texture.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
// Assumes pSurface is a valid IDirect3DVolume9 pointer
void *pContainer = NULL;
IDirect3DVolumeTexture9 *pVolumeTexture = NULL;
HRESULT hr = pVolume-&gt;GetContainer(IID_IDirect3DVolumeTexture9, &amp;pContainer);
if (SUCCEEDED(hr) &amp;&amp; pContainer)
{
    pVolumeTexture = (IDirect3DVolumeTexture9 *)pContainer;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b157d2d1-5813-43a1-ac3a-000b13b1bb62">IDirect3DVolume9</a>
 

 

