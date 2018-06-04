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

# IDirect3DDevice9::SetMaterial


## -description


Sets the material properties for the device.


## -parameters




### -param pMaterial [in]

Type: <b>const <a href="https://msdn.microsoft.com/943e6f6d-8091-462f-8c44-e0c27686934a">D3DMATERIAL9</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/943e6f6d-8091-462f-8c44-e0c27686934a">D3DMATERIAL9</a> structure, describing the material properties to set. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if the pMaterial parameter is invalid.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/834855f6-85ff-4c68-b1e7-8418042b71aa">IDirect3DDevice9::GetMaterial</a>
 

 

