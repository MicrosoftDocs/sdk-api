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

# _MESSAGE_RESOURCE_ENTRY structure


## -description


Contains the error message or message box display text for a message table resource. 


## -struct-fields




### -field Length

Type: <b>WORD</b>

The length, in bytes, of the <b>MESSAGE_RESOURCE_ENTRY</b> structure. 


### -field Flags

Type: <b>WORD</b>

Indicates that the string is encoded in Unicode, if equal to the value 0x0001. Indicates that the string is encoded in ANSI, if equal to the value 0x0000. 


### -field Text

Type: <b>BYTE[1]</b>

Pointer to an array that contains the error message or message box display text. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/573f22be-d204-4c0d-9c45-bd6d46094e32">MESSAGE_RESOURCE_BLOCK</a>



<a href="https://msdn.microsoft.com/439cf64e-29be-49ab-8bbf-cb98ac2e41cd">MESSAGE_RESOURCE_DATA</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

