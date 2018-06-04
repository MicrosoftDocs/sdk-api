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

# _WMT_BUFFER_SEGMENT structure


## -description



The <b>WMT_BUFFER_SEGMENT</b> structure contains the information needed to specify a segment in a buffer. It is used as a member of the <a href="https://msdn.microsoft.com/e1deb01f-9f53-4ede-a3e1-13d6dc79adb5">WMT_FILESINK_DATA_UNIT</a> and <a href="https://msdn.microsoft.com/5a99c772-0e8a-4f6d-a13f-9bf7b4fa7d89">WMT_PAYLOAD_FRAGMENT</a> structures to specify segments of a packet.




## -struct-fields




### -field pBuffer

Pointer to a buffer object containing the buffer segment.


### -field cbOffset

The offset, in bytes, from the start of the buffer to the buffer segment.


### -field cbLength

The length, in bytes, of the buffer segment.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

