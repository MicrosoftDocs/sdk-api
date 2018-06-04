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

# _DXVA2_DecodeExecuteParams structure


## -description



Contains parameters for the <a href="https://msdn.microsoft.com/3c957b2f-4bba-4c39-84de-719c08e1bf78">IDirectXVideoDecoder::Execute</a> method.




## -struct-fields




### -field NumCompBuffers

Number of compressed buffers.


### -field pCompressedBuffers

Pointer to an array of <a href="https://msdn.microsoft.com/eb17005a-035d-41cb-8f54-97b5d0f84736">DXVA2_DecodeBufferDesc</a> structures that describe the compressed buffers. The number of elements in the array is given by the <b>NumCompBuffers</b> member.


### -field pExtensionData

Pointer to a <a href="https://msdn.microsoft.com/2a1b7139-fcbb-40b0-9ed3-f9b1fe482358">DXVA2_DecodeExtensionData</a> structure that contains private data. Set this member to <b>NULL</b> unless you need to send private data to or from the driver.


## -see-also




<a href="https://msdn.microsoft.com/eb17005a-035d-41cb-8f54-97b5d0f84736">DXVA2_DecodeBufferDesc</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

