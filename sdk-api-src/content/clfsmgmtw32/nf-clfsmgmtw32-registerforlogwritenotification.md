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

# RegisterForLogWriteNotification function


## -description


The <b>RegisterForLogWriteNotification</b> function is 
    called by a managed log client to enable or disable log write notifications.


## -parameters




### -param hLog [in]

A handle to the log on which to resolve the log full condition.


### -param cbThreshold [in]

Number of bytes to be written to the log file before the notification is sent.


### -param fEnable [in]

If <b>TRUE</b>, the notification is enabled. If <b>FALSE</b>, the notification is disabled.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Valid values include the following:




## -see-also




<a href="https://msdn.microsoft.com/a8bcfdc6-3056-4f82-825b-f224100d87cb">CLFS Management Functions</a>
 

 

