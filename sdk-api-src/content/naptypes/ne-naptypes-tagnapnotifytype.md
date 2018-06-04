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

# tagNapNotifyType enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>Enumerates the types of service notifications sent by the NapAgent service. The NapAgent is also known as the Quarantine Agent.


## -enum-fields




### -field napNotifyTypeUnknown

Not used.


### -field napNotifyTypeServiceState

NapAgent service state change notifications. 

A notification of type <b>napNotifyTypeServiceState</b> is sent whenever the NapAgent service stops or starts.


### -field napNotifyTypeQuarState

Quarantine state change notifications. 

A notification of type <b>napNotifyTypeQuarState</b>  is sent whenever the isolation state changes. For more information, see <a href="https://msdn.microsoft.com/79f81e8e-a105-4cc9-b175-8a364648f3a6">IsolationState</a>.


## -see-also




<a href="https://msdn.microsoft.com/24180194-50d7-4f54-845d-25402af9cf9a">InitializeNapAgentNotifier</a>



<a href="https://msdn.microsoft.com/b676ee33-caf6-48f0-acf8-5be1b23c62fe">UninitializeNapAgentNotifier</a>
 

 

