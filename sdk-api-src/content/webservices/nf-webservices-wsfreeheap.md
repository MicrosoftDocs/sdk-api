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

# WsFreeHeap function


## -description



                This frees the heap object, and the memory associated with any allocations 
                made on it using <a href="https://msdn.microsoft.com/633b6a11-09ba-48a7-a1ad-940846c65d79">WsAlloc</a>.
            


## -parameters




### -param heap [in]


                    The heap to free.  This must be a valid heap object that was returned
                    from <a href="https://msdn.microsoft.com/459b7146-3b32-4df8-87e1-4ac7ad33ed0e">WsCreateHeap</a>.  This parameter may not be <b>NULL</b>.
                


## -returns



This function does not return a value.



