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

# PLOG_TAIL_ADVANCE_CALLBACK callback function


## -description


The 
<b>LOG_TAIL_ADVANCE_CALLBACK</b> function is an application-defined callback function that advances the log tail. The callback is invoked in the context of an asynchronous procedure call (APC) on the thread that registers for log management.


## -parameters




### -param hLogFile [in]

The handle to the log.


### -param lsnTarget [in]

Specifies the log sequence number (LSN) to which the client is advised to advance to or beyond. The <i>lsnTarget</i> may not refer to an actual record in the log.


### -param pvClientContext [in]

A pointer to the client context.


## -returns



This function does not return a value.




## -remarks



This callback can be invoked at any time. This callback function should advance the base LSN of the log to greater than or equal to the value of <i>lsnTarget</i>.




## -see-also




<a href="https://msdn.microsoft.com/aecdea3b-ac42-43d4-88b3-14cd810a4017">AdvanceLogBase</a>



<a href="https://msdn.microsoft.com/deb5fd90-e987-4e5b-9740-6ecef8705557">WriteLogRestartArea</a>
 

 

