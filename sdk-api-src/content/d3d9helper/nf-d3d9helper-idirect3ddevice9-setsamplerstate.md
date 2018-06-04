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

# IDirect3DDevice9::SetSamplerState


## -description


Sets the sampler state value.


## -parameters




### -param Sampler [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The sampler stage index. For more info about sampler stage, see <a href="vertex_textures_in_vs_3_0.htm">Sampling Stage Registers in vs_3_0 (DirectX HLSL)</a>.


### -param Type [in]

Type: <b><a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMPLERSTATETYPE</a></b>

This parameter can be any member of the <a href="https://msdn.microsoft.com/03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0">D3DSAMPLERSTATETYPE</a> enumerated type. 


### -param Value [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

State value to set. The meaning of this value is determined by the Type parameter. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/497305c9-7cbf-4aee-9a83-dddfdd9014ae">IDirect3DDevice9::GetSamplerState</a>
 

 

