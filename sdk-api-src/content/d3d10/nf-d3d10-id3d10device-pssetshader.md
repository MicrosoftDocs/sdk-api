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

# ID3D10Device::PSSetShader


## -description


Sets a pixel shader to the device.


## -parameters




### -param pPixelShader [in]

Type: <b><a href="https://msdn.microsoft.com/c2b255ca-cffb-4e24-9395-a4cb727bf421">ID3D10PixelShader</a>*</b>

Pointer to a pixel shader (see <a href="https://msdn.microsoft.com/c2b255ca-cffb-4e24-9395-a4cb727bf421">ID3D10PixelShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.


## -returns



Returns nothing.




## -remarks



The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

