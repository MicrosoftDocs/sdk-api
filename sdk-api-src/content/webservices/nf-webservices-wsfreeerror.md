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

# WsFreeError function


## -description


Releases the memory resource associated with an   <b>Error</b> object created using  <a href="https://msdn.microsoft.com/0ec858f7-12a5-43cf-94a7-3838ab6d76ae">WsCreateError</a>.
            This releases the object and its constituent information.
            


## -parameters




### -param error [in]


                    A pointer to the <b>Error</b> object to release.  The pointer must reference a valid <b>WS_ERROR</b> object
                    returned by <a href="https://msdn.microsoft.com/0ec858f7-12a5-43cf-94a7-3838ab6d76ae">WsCreateError</a>.  The referenced value may 
                    not be NULL.
                


## -returns



This function does not return a value.



