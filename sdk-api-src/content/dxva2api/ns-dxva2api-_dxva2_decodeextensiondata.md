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

# _DXVA2_DecodeExtensionData structure


## -description



Contains private data for the <a href="https://msdn.microsoft.com/3c957b2f-4bba-4c39-84de-719c08e1bf78">IDirectXVideoDecoder::Execute</a> method.




## -struct-fields




### -field Function

Function number. This can be zero if this argument is the default or is ignored.


### -field pPrivateInputData

Pointer to private input data passed to the driver.


### -field PrivateInputDataSize

Length of the private input data, in bytes.


### -field pPrivateOutputData

Pointer to private output data passed from the driver to the decoder.


### -field PrivateOutputDataSize

Size of the private output data, in bytes.


## -remarks



This structure corresponds to parameters of the <b>IAMVideoAccelerator::Execute</b> method in DirectX Video Acceleration (DXVA) version 1.




## -see-also




<a href="https://msdn.microsoft.com/e0e95e9b-6d53-4b90-a933-243023dc31ef">DXVA2_DecodeExecuteParams</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

