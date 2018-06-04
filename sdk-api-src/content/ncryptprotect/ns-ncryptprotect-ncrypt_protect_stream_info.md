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

# NCRYPT_PROTECT_STREAM_INFO structure


## -description


The <b>NCRYPT_PROTECT_STREAM_INFO</b> structure is used by the <a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a> and <a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a> functions to pass blocks of processed data to your application.


## -struct-fields




### -field pfnStreamOutput

Address of a callback function that accepts data from the stream encryption or decryption process. for more information, see <a href="https://msdn.microsoft.com/D07B2B63-306B-4C41-AA14-320EFEFFB939">PFNCryptStreamOutputCallback</a>.


### -field pvCallbackCtxt

Pointer to a buffer supplied the caller. The buffer is not modified by the data protection API. You can use the buffer to keep track of your application.


## -see-also




<a href="https://msdn.microsoft.com/7DE74BB1-1B84-4721-BE4A-4D2661E93E00">NCryptStreamOpenToProtect</a>



<a href="https://msdn.microsoft.com/9848082E-EDDA-4DA1-9896-42EAF2ADFAB4">NCryptStreamOpenToUnprotect</a>



<a href="https://msdn.microsoft.com/D07B2B63-306B-4C41-AA14-320EFEFFB939">PFNCryptStreamOutputCallback</a>
 

 

