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

# DrtUnregisterKey function


## -description


The <b>DrtUnregisterKey</b> function deregisters a key from the DRT.


## -parameters




### -param hKeyRegistration [in]

The DRT handle returned by the <a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a> function specifying a registered key within the DRT.


## -returns



This function does not return a value.




## -remarks



A node can deregister a key anytime after registration.  Additionally, if an application calls <a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a>, all keys are deregistered by the DRT infrastructure.

Only the application that registered they key may deregister it. An application can deregister a key from the local node. Upon completion the function triggers a <b>DRT_EVENT_LEAFSET_KEY_CHANGE</b> event;  informing the application and other nodes participating in the DRT mesh of the deregistration. 




## -see-also




<a href="https://msdn.microsoft.com/37c0a579-64be-4ed6-b1b3-852013875361">DrtClose</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>



<a href="https://msdn.microsoft.com/9aa1ee16-648d-4769-a464-4659dea14dba">DrtRegisterKey</a>
 

 

