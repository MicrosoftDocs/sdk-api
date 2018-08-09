---
UID: NF:d3d9helper.IDirect3DSurface9.GetContainer
title: IDirect3DSurface9::GetContainer
author: windows-sdk-content
description: Provides access to the parent cube texture or texture (mipmap) object, if this surface is a child level of a cube texture or a mipmap. This method can also provide access to the parent swap chain if the surface is a back-buffer child.
old-location: direct3d9\idirect3dsurface9__getcontainer.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getcontainer.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetContainer, GetContainer method [Direct3D 9], GetContainer method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetContainer method, IDirect3DSurface9.GetContainer, IDirect3DSurface9::GetContainer, b487bd6c-1138-b391-b264-d95eb2cadb18, d3d9helper/IDirect3DSurface9::GetContainer, direct3d9.idirect3dsurface9__getcontainer
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DSurface9.GetContainer
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
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
 

 

