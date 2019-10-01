---
UID: NF:d3d9.IDirect3DDevice9.GetViewport
title: IDirect3DDevice9::GetViewport (d3d9.h)
author: windows-sdk-content
description: Retrieves the viewport parameters currently set for the device.
old-location: direct3d9\idirect3ddevice9__getviewport.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getviewport.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 5804c163-148c-f385-7d81-0260f741a050, GetViewport, GetViewport method [Direct3D 9], GetViewport method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetViewport method, IDirect3DDevice9.GetViewport, IDirect3DDevice9::GetViewport, d3d9helper/IDirect3DDevice9::GetViewport, direct3d9.idirect3ddevice9__getviewport
ms.topic: method
f1_keywords: 
 - "d3d9/IDirect3DDevice9.GetViewport"
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
 - IDirect3DDevice9.GetViewport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DDevice9::GetViewport


## -description


Retrieves the viewport parameters currently set for the device.


## -parameters




### -param pViewport [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dviewport9">D3DVIEWPORT9</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/direct3d9/d3dviewport9">D3DVIEWPORT9</a> structure, representing the returned viewport parameters. 


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the pViewport parameter is invalid.




## -remarks



Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport">IDirect3DDevice9::SetViewport</a>
 

 

