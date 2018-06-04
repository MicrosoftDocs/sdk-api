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

# IDirect3DDevice9::CreatePixelShader


## -description


Creates a pixel shader.


## -parameters




### -param pFunction [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

Pointer to the pixel shader function token array, specifying the blending operations. This value cannot be <b>NULL</b>. 


### -param ppShader [out, retval]

Type: <b><a href="https://msdn.microsoft.com/b199544d-4617-4fe2-8a4a-d54fabd4d449">IDirect3DPixelShader9</a>**</b>

Pointer to the returned pixel shader interface. See <a href="https://msdn.microsoft.com/b199544d-4617-4fe2-8a4a-d54fabd4d449">IDirect3DPixelShader9</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, 
E_OUTOFMEMORY.




## -see-also




<a href="https://msdn.microsoft.com/24c3dcae-9397-4856-b072-0ae340157bf9">D3DXAssembleShader</a>



<a href="https://msdn.microsoft.com/2977b64a-b8cc-454b-8e28-291f6f2c6fc1">D3DXAssembleShaderFromFile</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

