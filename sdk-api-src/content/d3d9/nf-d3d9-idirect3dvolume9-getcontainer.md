---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

