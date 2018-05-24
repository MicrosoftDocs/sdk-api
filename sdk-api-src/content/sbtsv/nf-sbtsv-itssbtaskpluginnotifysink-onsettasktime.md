---
UID: NF:sbtsv.ITsSbTaskPluginNotifySink.OnSetTaskTime
title: ITsSbTaskPluginNotifySink::OnSetTaskTime
author: windows-driver-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that a task has been scheduled.
old-location: termserv\itssbtaskpluginnotifysink_onsettasktime.htm
old-project: TermServ
ms.assetid: 6f9b58ba-8cda-4f8d-9c23-19475262148c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITsSbTaskPluginNotifySink interface [Remote Desktop Services],OnSetTaskTime method, ITsSbTaskPluginNotifySink.OnSetTaskTime, ITsSbTaskPluginNotifySink::OnSetTaskTime, OnSetTaskTime, OnSetTaskTime method [Remote Desktop Services], OnSetTaskTime method [Remote Desktop Services],ITsSbTaskPluginNotifySink interface, sbtsv/ITsSbTaskPluginNotifySink::OnSetTaskTime, termserv.itssbtaskpluginnotifysink_onsettasktime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbTaskPluginNotifySink.OnSetTaskTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

