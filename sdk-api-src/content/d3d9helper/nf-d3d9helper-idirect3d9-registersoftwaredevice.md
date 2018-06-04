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

# IDirect3D9::RegisterSoftwareDevice


## -description


Registers a pluggable software device. Software devices provide software rasterization enabling applications to access a variety of software rasterizers.


## -parameters




### -param pInitializeFunction [in]

Type: <b>void*</b>

Pointer to the initialization function for the software device to be registered. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL. The method call is invalid. For example, a method's parameter may have an invalid value: D3DERR_OUTOFVIDEOMEMORY. 




## -remarks



If the user's computer provides no special hardware acceleration for 3D operations, your application might emulate 3D hardware in software. Software rasterization devices emulate the functions of color 3D hardware in software. A software device runs more slowly than a hal. However, software devices
    
    take advantage of any special instructions supported by the CPU to increase performance. Instruction sets include the AMD 3DNow! instruction set on some AMD processors and the MMX instruction set supported by many Intel processors. Direct3D uses the 3D-Now! instruction set to accelerate transformation and lighting operations and the MMX instruction set to accelerate rasterization.

Software devices communicate with Direct3D through an interface similar to the hardware device driver interface (DDI).

Software devices are loaded by the application and registered with the <a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a> object. Direct3D uses the software device for rendering. 

The Direct3D Driver Development Kit (DDK) provides the documentation and headers for developing pluggable software devices.




## -see-also




<a href="https://msdn.microsoft.com/af321e4f-aaff-4285-bdac-9aab5c1dc5d8">IDirect3D9</a>
 

 

