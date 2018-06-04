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

# ITAllocatorProperties::SetAllocatorProperties


## -description


The 
<b>SetAllocatorProperties</b> method must be called before connection and will force the MSP to use these values during filter negotiation. If the connecting filter doesn't accept these values, the connection is not established.


## -parameters




### -param pAllocProperties [in]

Pointer to the allocator buffer.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an error value.




## -remarks



<b>This method should be used with extreme care.</b> The quality of the sound may suffer if the values entered for this method are not optimal for the MSP. Therefore, the application should know exactly the properties preferred by the MSP before calling this method. Under Windows 2000, properties entered during calls to this method are ignored if they are not optimal. Under Windows XP, these values are not ignored and the application must be more knowledgeable.

If the application is only concerned with setting consistent buffer sizes, the 
<a href="https://msdn.microsoft.com/5aea70fd-2078-4f51-909f-c51cb997f5ea">ITAllocatorProperties::SetBufferSize</a> method should be used instead. This guarantees the application is provided with the specified buffer size.




## -see-also




<a href="https://msdn.microsoft.com/a0facf08-1b03-415b-b97e-3fda5a164b89">ITAllocatorProperties</a>
 

 

