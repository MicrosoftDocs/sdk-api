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

# ITsSbTaskPluginNotifySink::OnSetTaskTime


## -description


Notifies Remote Desktop Connection Broker (RD Connection Broker) that a task has been scheduled.


## -parameters




### -param szTargetName [in]

The name of the target.


### -param TaskStartTime [in]

A <b>FILETIME</b> structure specifying the start time (UTC).


### -param TaskEndTime [in]

A <b>FILETIME</b> structure specifying the end time (UTC).


### -param TaskDeadline [in]

A <b>FILETIME</b> structure specifying the deadline (UTC).


### -param szTaskLabel [in]

A label describing the purpose of the task.


### -param szTaskIdentifier [in]

Identifies the target.


### -param szTaskPlugin [in]

The display name of the task agent.


### -param dwTaskStatus [in]

An <a href="https://msdn.microsoft.com/69278A29-9100-4855-B5B3-C790563B8B72">RDV_TASK_STATUS</a> enumeration value  that represents the state of the task.


### -param saContext [in]

The context bytes associated with the task.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc1b56f3-ea5f-4df5-b90a-ce24c36aee21">ITsSbTaskPluginNotifySink</a>
 

 

