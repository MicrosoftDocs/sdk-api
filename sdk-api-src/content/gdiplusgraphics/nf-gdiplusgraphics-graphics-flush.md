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

# Graphics::Flush


## -description


The <b>Graphics::Flush</b> method flushes all pending graphics operations. 


## -parameters




### -param intention [in]

Type: <b><a href="https://msdn.microsoft.com/fa08d76e-c1fb-4abb-9770-93f3ae01a066">FlushIntention</a></b>

Element of the <a href="https://msdn.microsoft.com/fa08d76e-c1fb-4abb-9770-93f3ae01a066">FlushIntention</a> enumeration that specifies whether pending operations are flushed immediately (not executed) or executed as soon as possible. 


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/fa08d76e-c1fb-4abb-9770-93f3ae01a066">FlushIntention</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>
 

 

