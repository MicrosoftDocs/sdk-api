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

# XAPO_BUFFER_FLAGS enumeration


## -description


Describes the contents of a stream buffer. 


## -enum-fields




### -field XAPO_BUFFER_SILENT

Stream buffer contains only silent samples.


### -field XAPO_BUFFER_VALID

Stream buffer contains audio data to be processed.


## -remarks



This metadata can be used to implement optimizations that require knowledge of a stream buffer's contents. For example, XAPOs that always produce silent output from silent input can check the flag on the input stream buffer to determine if any signal processing is necessary. If silent, the XAPO can simply set the flag on the output stream buffer to silent and return, thus averting the work of processing silent data.



Likewise, XAPOs that receive valid input data, but generate silence (for any reason), may set the output stream buffer's flag accordingly, rather than writing silent samples to the buffer.



These flags represent what should be assumed is in the respective buffer. The flags may not reflect what is actually stored in memory. For example, the XAPO_BUFFER_SILENT indicates that silent data should be assumed, however the respective memory may be uninitialized



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/7b20bda9-dab2-cfbc-125a-cf46e4ede0c8">Enumerations</a>
 

 

