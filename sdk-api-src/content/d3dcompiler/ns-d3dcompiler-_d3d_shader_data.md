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

# _D3D_SHADER_DATA structure


## -description


Describes shader data.


## -struct-fields




### -field pBytecode

A pointer to shader data.


### -field BytecodeLength

Length of shader data that <b>pBytecode</b> points to.


## -remarks



An array of <b>D3D_SHADER_DATA</b> structures is passed to <a href="https://msdn.microsoft.com/e53a0d36-3cd4-4327-8969-6a864b38a15b">D3DCompressShaders</a> to compress the shader data into a more compact form.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

