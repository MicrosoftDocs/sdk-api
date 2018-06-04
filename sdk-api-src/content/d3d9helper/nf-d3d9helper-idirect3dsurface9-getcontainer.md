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

# IDirect3DSurface9::GetContainer


## -description


Provides access to the parent cube texture or texture (mipmap) object, if this surface is a child level of a cube texture or a mipmap. This method can also provide access to the parent swap chain if the surface is a back-buffer child.


## -parameters




### -param riid [in]

Type: <b>REFIID</b>

Reference identifier of the container being requested. 


### -param ppContainer [out]

Type: <b>void**</b>

Address of a pointer to fill with the container pointer if the query succeeds. See Remarks. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



If the surface is created using <a href="https://msdn.microsoft.com/3c0c8651-0c54-4eeb-bd37-c2aa26b1211d">CreateRenderTarget</a> or <a href="https://msdn.microsoft.com/9502aa34-afde-4547-a5da-224f29719c07">CreateOffscreenPlainSurface</a> or <a href="https://msdn.microsoft.com/c94eed81-0706-44d6-a8be-83e2a5d46c39">CreateDepthStencilSurface</a>, the surface is considered stand alone. In this case, <b>GetContainer</b> will return the Direct3D device used to create the surface.

If the call succeeds, the reference count of the container is increased by one.

Here's an example getting the parent texture of a mip surface.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
    
// Assumes pSurface is a valid IDirect3DSurface9 pointer
void *pContainer = NULL;
IDirect3DTexture9 *pTexture = NULL;
HRESULT hr = pSurface-&gt;GetContainer(IID_IDirect3DTexture9, &amp;pContainer);
if (SUCCEEDED(hr) &amp;&amp; pContainer)
{
    pTexture = (IDirect3DTexture9 *)pContainer;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>
 

 

