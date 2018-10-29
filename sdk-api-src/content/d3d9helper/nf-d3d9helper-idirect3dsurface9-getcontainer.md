---
UID: NF:d3d9helper.IDirect3DSurface9.GetContainer
title: IDirect3DSurface9::GetContainer
author: windows-sdk-content
description: Provides access to the parent cube texture or texture (mipmap) object, if this surface is a child level of a cube texture or a mipmap. This method can also provide access to the parent swap chain if the surface is a back-buffer child.
old-location: direct3d9\idirect3dsurface9__getcontainer.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getcontainer.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetContainer, GetContainer method [Direct3D 9], GetContainer method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetContainer method, IDirect3DSurface9.GetContainer, IDirect3DSurface9::GetContainer, b487bd6c-1138-b391-b264-d95eb2cadb18, d3d9helper/IDirect3DSurface9::GetContainer, direct3d9.idirect3dsurface9__getcontainer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



If the surface is created using <a href="https://msdn.microsoft.com/en-us/library/Bb174361(v=VS.85).aspx">CreateRenderTarget</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb174358(v=VS.85).aspx">CreateOffscreenPlainSurface</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb174356(v=VS.85).aspx">CreateDepthStencilSurface</a>, the surface is considered stand alone. In this case, <b>GetContainer</b> will return the Direct3D device used to create the surface.

If the call succeeds, the reference count of the container is increased by one.

Here's an example getting the parent texture of a mip surface.


```

    
// Assumes pSurface is a valid IDirect3DSurface9 pointer
void *pContainer = NULL;
IDirect3DTexture9 *pTexture = NULL;
HRESULT hr = pSurface->GetContainer(IID_IDirect3DTexture9, &pContainer);
if (SUCCEEDED(hr) && pContainer)
{
    pTexture = (IDirect3DTexture9 *)pContainer;
}

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205892(v=VS.85).aspx">IDirect3DSurface9</a>
 

 

