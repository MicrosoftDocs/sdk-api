---
UID: NF:d3d9helper.IDirect3DDevice9.GetVertexShader
title: IDirect3DDevice9::GetVertexShader
author: windows-sdk-content
description: Retrieves the currently set vertex shader.
old-location: direct3d9\idirect3ddevice9__getvertexshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getvertexshader.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetVertexShader, GetVertexShader method [Direct3D 9], GetVertexShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetVertexShader method, IDirect3DDevice9.GetVertexShader, IDirect3DDevice9::GetVertexShader, ce5c5bb1-c3dc-79d2-8932-365b84538ce0, d3d9helper/IDirect3DDevice9::GetVertexShader, direct3d9.idirect3ddevice9__getvertexshader
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
 - IDirect3DDevice9.GetVertexShader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetVertexShader


## -description


Retrieves the currently set vertex shader.


## -parameters




### -param ppShader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/834bd54b-673b-4fa8-aba5-30ed5b923542">IDirect3DVertexShader9</a>**</b>

Pointer to a vertex shader interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 If ppShader is invalid, D3DERR_INVALIDCALL is returned.




## -remarks



Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device because it returns an interface.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e4913fd8-5cb3-4799-8c91-d39f213d4b47">IDirect3DDevice9::SetVertexShader</a>
 

 

