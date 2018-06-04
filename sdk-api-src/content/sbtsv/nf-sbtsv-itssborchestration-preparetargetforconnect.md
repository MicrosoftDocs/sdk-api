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

# ITsSbOrchestration::PrepareTargetForConnect


## -description


Prepares the target for a client connection.


## -parameters




### -param pConnection [in]

 A pointer to an <a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a> client connection object.


### -param pOrchestrationNotifySink [in]

A pointer to an <a href="https://msdn.microsoft.com/767b6e73-ee0d-4802-99ff-ac37880a0884">ITsSbOrchestrationNotifySink</a> orchestration notify sink object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is particularly useful for plug-ins that redirect users to virtual desktops. Remote Desktop Connection Broker (RD Connection Broker) 
calls this method after placement has successfully completed. Orchestration can 
include waking a virtual machine and determining its IP address. Your implementation of this method should ensure that the target is ready to accept a client connection.




## -see-also




<a href="https://msdn.microsoft.com/6649f43d-0e2a-42d7-8111-862bb28e3dbc">ITsSbClientConnection</a>



<a href="https://msdn.microsoft.com/fae858ae-19e5-453d-b9ef-1da7ea706e49">ITsSbOrchestration</a>



<a href="https://msdn.microsoft.com/767b6e73-ee0d-4802-99ff-ac37880a0884">ITsSbOrchestrationNotifySink</a>
 

 

