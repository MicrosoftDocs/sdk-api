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

# ID3D11DeviceContext1::CSGetConstantBuffers1


## -description


Gets the constant buffers that the compute-shader stage uses.


## -parameters




### -param StartSlot [in]

Index into the device's zero-based array to begin retrieving constant buffers from (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - 1).


### -param NumBuffers [in]

Number of buffers to retrieve (ranges from 0 to D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT - <i>StartSlot</i>).


### -param ppConstantBuffers [out, optional]

Array of constant buffer interface pointers to be returned by the method.


### -param pFirstConstant [out, optional]

A pointer to an array that receives the offsets into the buffers that  <i>ppConstantBuffers</i> specifies. Each offset specifies where, from the shader's point of view, each constant buffer starts.  Each offset is measured in shader constants, which are 16 bytes (4*32-bit components).  Therefore, an offset of 2 indicates that the start of the associated constant buffer is 32 bytes into the constant buffer. The runtime sets <i>pFirstConstant</i> to <b>NULL</b> if the buffers do not have offsets.


### -param pNumConstants [out, optional]

A pointer to an array that receives the numbers of constants in the buffers that  <i>ppConstantBuffers</i> specifies. Each number specifies the number of constants that are contained in the constant buffer that the shader uses. Each number of constants starts from its respective offset that is specified in the <i>pFirstConstant</i> array. The runtime sets <i>pNumConstants</i> to <b>NULL</b> if it doesn't specify the numbers of constants in each buffer.


## -returns



Returns nothing.




## -remarks



If no buffer is bound at a slot, <i>pFirstConstant</i> and <i>pNumConstants</i> are <b>NULL</b> for that slot.




## -see-also




<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

