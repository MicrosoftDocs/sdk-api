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
 

 

