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

# lineShutdown function


## -description


The 
<b>lineShutdown</b> function shuts down the application's usage of the line abstraction of the API.


## -parameters




### -param hLineApp

Application's usage handle for the line API.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -remarks



If this function is called when the application has lines open or calls active, the call handles are deleted and TAPI automatically performs the equivalent of a 
<a href="https://msdn.microsoft.com/ec47a351-c693-4e71-bf23-c31110ca90a1">lineClose</a> on each open line. However, it is recommended that applications explicitly close all open lines before invoking 
<b>lineShutdown</b>. If shutdown is performed while asynchronous requests are outstanding, those requests are canceled.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/ec47a351-c693-4e71-bf23-c31110ca90a1">lineClose</a>
 

 

