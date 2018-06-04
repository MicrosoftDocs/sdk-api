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

# IDirect3DDevice9::GetCreationParameters


## -description


Retrieves the creation parameters of the device.


## -parameters




### -param pParameters [out]

Type: <b><a href="https://msdn.microsoft.com/7db5ef2b-6894-4113-b726-8b238bb4fb2f">D3DDEVICE_CREATION_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/7db5ef2b-6894-4113-b726-8b238bb4fb2f">D3DDEVICE_CREATION_PARAMETERS</a> structure, describing the creation parameters of the device. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.


D3DERR_INVALIDCALL is returned if the argument is invalid.




## -remarks



You can query the AdapterOrdinal member of the returned <a href="https://msdn.microsoft.com/7db5ef2b-6894-4113-b726-8b238bb4fb2f">D3DDEVICE_CREATION_PARAMETERS</a> structure to retrieve the ordinal of the adapter represented by this device. 




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

