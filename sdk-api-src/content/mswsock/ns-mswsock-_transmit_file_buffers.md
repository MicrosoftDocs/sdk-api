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

# _TRANSMIT_FILE_BUFFERS structure


## -description



			The 
<b>TRANSMIT_FILE_BUFFERS</b> structure specifies data to be transmitted before and after file data during a 
<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a> function file transfer operation.


## -struct-fields




### -field Head

Pointer to a buffer that contains data to be transmitted before the file data is transmitted.


### -field HeadLength

Size of the buffer pointed to by <b>Head</b>, in bytes, to be transmitted.


### -field Tail

Pointer to a buffer that contains data to be transmitted after the file data is transmitted.


### -field TailLength

Size of the buffer pointed to <b>Tail</b>, in bytes, to be transmitted.


## -see-also




<a href="https://msdn.microsoft.com/45db763e-735d-48ac-a0e4-6e63b5dda7a5">TransmitFile</a>
 

 

