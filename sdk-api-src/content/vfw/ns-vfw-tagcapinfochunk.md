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

# tagCapInfoChunk structure


## -description



The <b>CAPINFOCHUNK</b> structure contains parameters that can be used to define an information chunk within an AVI capture file. The <a href="https://msdn.microsoft.com/67d11a05-a2b4-45d2-ba66-83a198745303">WM_CAP_FILE_SET_INFOCHUNK</a> message or <b>capSetInfoChunk</b> macro is used to send a <b>CAPINFOCHUNK</b> structure to a capture window.




## -struct-fields




### -field fccInfoID

Four-character code that identifies the representation of the chunk data. If this value is <b>NULL</b> and <b>lpData</b> is <b>NULL</b>, all accumulated information chunks are deleted.


### -field lpData

Pointer to the data. If this value is <b>NULL</b>, all <b>fccInfoID</b> information chunks are deleted.


### -field cbData

Size, in bytes, of the data pointed to by <b>lpData</b>. If <b>lpData</b> specifies a null-terminated string, use the string length incremented by one to save the <b>NULL</b> with the string.


## -see-also




Video Capture



<a href="https://msdn.microsoft.com/180010d2-240e-433d-b306-341b9b1e0b57">Video Capture Structures</a>



<a href="https://msdn.microsoft.com/67d11a05-a2b4-45d2-ba66-83a198745303">WM_CAP_FILE_SET_INFOCHUNK</a>
 

 

