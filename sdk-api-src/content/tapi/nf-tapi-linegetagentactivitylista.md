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

# lineGetAgentActivityListA function


## -description


The 
<b>lineGetAgentActivityList</b> function obtains the identities of activities that the application can select using 
<a href="https://msdn.microsoft.com/2c46e1cb-e2d7-4cb5-b937-55011058fd15">lineSetAgentActivity</a> to indicate what function the agent is actually performing at the moment.


## -parameters




### -param hLine

Handle to the open line device.


### -param dwAddressID

Address on the open line device whose agent status is to be queried. An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.


### -param lpAgentActivityList

Pointer to a variably sized structure of type 
<a href="https://msdn.microsoft.com/61e46717-8a14-440f-bb61-991c3dadd778">LINEAGENTACTIVITYLIST</a>. Upon successful completion of the request, this structure is filled with a list of the agent activity codes that can be selected using 
<a href="https://msdn.microsoft.com/2c46e1cb-e2d7-4cb5-b937-55011058fd15">lineSetAgentActivity</a>. Prior to calling 
<b>lineGetAgentActivityList</b>, the application should set the <b>dwTotalSize</b> member of this structure to indicate the amount of memory available to TAPI for returning information.


## -returns



Returns a positive request identifier if the asynchronous operation starts; otherwise, this function returns one of these negative error values:

LINEERR_INVALADDRESSID, LINEERR_OPERATIONFAILED, LINEERR_INVALAGENTID, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALLINEHANDLE, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_STRUCTURETOOSMALL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.




## -see-also




<a href="https://msdn.microsoft.com/61e46717-8a14-440f-bb61-991c3dadd778">LINEAGENTACTIVITYLIST</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/2c46e1cb-e2d7-4cb5-b937-55011058fd15">lineSetAgentActivity</a>
 

 

