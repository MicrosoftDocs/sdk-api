---
UID: NF:d3d9.IDirect3DVertexShader9.GetFunction
title: IDirect3DVertexShader9::GetFunction
author: windows-sdk-content
description: Gets a pointer to the shader data.
old-location: direct3d9\idirect3dvertexshader9__getfunction.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvertexshader9__getfunction.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: GetFunction, GetFunction method [Direct3D 9], GetFunction method [Direct3D 9],IDirect3DVertexShader9 interface, IDirect3DVertexShader9 interface [Direct3D 9],GetFunction method, IDirect3DVertexShader9.GetFunction, IDirect3DVertexShader9::GetFunction, d0abe93b-084e-be3d-d4c2-e12b15c9898f, d3d9helper/IDirect3DVertexShader9::GetFunction, direct3d9.idirect3dvertexshader9__getfunction
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
 - IDirect3DVertexShader9.GetFunction
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVertexShader9::GetFunction


## -description


Gets a pointer to the shader data.


## -parameters




### -param param




### -param pSizeOfData [in, out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Size of the data, in bytes. To get the buffer size that is needed to retrieve the data, set pData = <b>NULL</b> when calling GetFunction. Then call GetFunction with the returned size, to get the buffer data.


#### - pData [in, out]

Type: <b>void*</b>

Pointer to a buffer that contains the shader data. The application needs to allocate enough room for this. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/834bd54b-673b-4fa8-aba5-30ed5b923542">IDirect3DVertexShader9</a>
 

 

