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

# ISdoServiceControl::GetServiceStatus


## -description


The <b>GetServiceStatus</b> method 
    retrieves the status of the service being administered through SDO.


## -parameters




### -param status [out]

Pointer to a <b>LONG</b> variable that contains the status of the service. The status 
      is one of the following values.



#### SERVICE_STOPPED

The service is stopped.



#### SERVICE_START_PENDING

The service is starting.



#### SERVICE_STOP_PENDING

The service is shutting down.



#### SERVICE_RUNNING

The service is up and running.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/265f034a-78be-4792-958e-80ad7a71d1a7">ISdoMachine::GetServiceSDO</a>



<a href="https://msdn.microsoft.com/c901ac9a-524a-498d-8b72-9afb26cf2c58">ISdoServiceControl</a>
 

 

