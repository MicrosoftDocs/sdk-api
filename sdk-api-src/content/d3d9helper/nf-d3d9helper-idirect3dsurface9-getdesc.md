---
UID: NF:d3d9helper.IDirect3DSurface9.GetDesc
title: IDirect3DSurface9::GetDesc
author: windows-sdk-content
description: Retrieves a description of the surface.
old-location: direct3d9\idirect3dsurface9__getdesc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__getdesc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 068aa9b6-08d4-5e72-dc9f-18e83e42aef2, GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DSurface9 interface, IDirect3DSurface9 interface [Direct3D 9],GetDesc method, IDirect3DSurface9.GetDesc, IDirect3DSurface9::GetDesc, d3d9helper/IDirect3DSurface9::GetDesc, direct3d9.idirect3dsurface9__getdesc
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
 - IDirect3DSurface9.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSurface9::GetDesc


## -description


Retrieves a description of the surface.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/fad8ffdb-36e5-4695-b343-e1315357c31a">D3DSURFACE_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/fad8ffdb-36e5-4695-b343-e1315357c31a">D3DSURFACE_DESC</a> structure, describing the surface. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.

D3DERR_INVALIDCALL is returned if the argument is invalid.




## -see-also




<a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>
 

 

