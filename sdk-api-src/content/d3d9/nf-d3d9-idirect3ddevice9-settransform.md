---
UID: NF:d3d9.IDirect3DDevice9.SetTransform
title: IDirect3DDevice9::SetTransform
author: windows-sdk-content
description: Sets a single device transformation-related state.
old-location: direct3d9\idirect3ddevice9__settransform.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settransform.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 25042e52-3212-5250-0bac-ab23f76aaeb1, IDirect3DDevice9 interface [Direct3D 9],SetTransform method, IDirect3DDevice9.SetTransform, IDirect3DDevice9::SetTransform, SetTransform, SetTransform method [Direct3D 9], SetTransform method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTransform, direct3d9.idirect3ddevice9__settransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.SetTransform
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetTransform


## -description


Sets a single device transformation-related state.


## -parameters




### -param State [in]

Type: <b><a href="https://msdn.microsoft.com/53535d9f-246a-42cf-82a2-fb3cf6d4ebac">D3DTRANSFORMSTATETYPE</a></b>

Device-state variable that is being modified. This parameter can be any member of the <a href="https://msdn.microsoft.com/53535d9f-246a-42cf-82a2-fb3cf6d4ebac">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro. 


### -param pMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a> structure that modifies the current transformation. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one of the arguments is invalid.




## -see-also




<a href="https://msdn.microsoft.com/2bf7ac8a-43d8-460e-a400-3b33e96441db">D3DTS_WORLD</a>



<a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a>



<a href="https://msdn.microsoft.com/cab444c2-b245-4d1a-a90c-745c92a2ea89">D3DTS_WORLDn</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/0e91cdfc-27d7-481f-b0e0-f89f0049ffce">IDirect3DDevice9::GetTransform</a>



<a href="https://msdn.microsoft.com/65738aae-aa90-48c5-8c9c-1927d1c92c54">IDirect3DDevice9::SetRenderState</a>
 

 

