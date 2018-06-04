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

# TokenBindingGetKeyTypesClient function


## -description


Retrieves a list of the key types that the client device supports.


## -parameters




### -param keyTypes [out]

A pointer to a buffer that contains the list of key types that the client device supports. <b>TokenBindingGetKeyTypesClient</b> returns the string identifiers for well-known algorithms that correspond to the keys that the client device supports. Use <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> to allocate the memory for the buffer, and <a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a> to free that memory. 


## -returns



Returns a status code that indicates the success or failure of the function.




## -remarks



You can call <b>TokenBindingGetKeyTypesClient</b> from user mode.




## -see-also




<a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a>



<a href="https://msdn.microsoft.com/6139e55f-9dda-42b5-bc9b-8d9bbfeaa619">HeapFree</a>



<a href="https://msdn.microsoft.com/E5029CE3-CD23-4566-A951-35374DC7BC57">TOKENBINDING_KEY_TYPES</a>



<a href="https://msdn.microsoft.com/8ABAC0AF-AF68-4742-9C36-3FB17D303409">TokenBindingGetKeyTypesServer</a>
 

 

