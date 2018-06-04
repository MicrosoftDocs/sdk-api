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

# AVIFileInit function


## -description



The <b>AVIFileInit</b> function initializes the AVIFile library.



The AVIFile library maintains a count of the number of times it is initialized, but not the number of times it was released. Use the <a href="https://msdn.microsoft.com/2daa509a-9e95-4f49-8195-97d3e7cd17b4">AVIFileExit</a> function to release the AVIFile library and decrement the reference count. Call <b>AVIFileInit</b> before using any other AVIFile functions.

This function supersedes the obsolete <b>AVIStreamInit</b> function.


## -parameters






## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/89abf60a-1714-4836-93ae-a8a6bf2c24b6">AVIFile Functions</a>



<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>
 

 

