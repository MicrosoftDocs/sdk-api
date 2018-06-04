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

# AVIStreamCreate function


## -description



The <b>AVIStreamCreate</b> function creates a stream not associated with any file.




## -parameters




### -param ppavi

Pointer to a buffer that receives the new stream interface.


### -param lParam1

Stream-handler specific information.


### -param lParam2

Stream-handler specific information.


### -param pclsidHandler

Pointer to the class identifier used for the stream.


## -returns



Returns zero if successful or an error otherwise.




## -remarks



You should not need to call this function. Some functions, such as <a href="https://msdn.microsoft.com/9c7b0ebe-c113-49c9-a74f-61f47e7c18af">CreateEditableStream</a> and <a href="https://msdn.microsoft.com/63279d7e-0e64-4708-a29c-60d5fdf75cb2">AVIMakeCompressedStream</a>, use it internally.

The argument <i>ppavi</i> contains the address of a pointer to an <a href="https://msdn.microsoft.com/25f67f04-e005-48ee-89e7-a6ef89f6d6c6">IAVIStream</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

