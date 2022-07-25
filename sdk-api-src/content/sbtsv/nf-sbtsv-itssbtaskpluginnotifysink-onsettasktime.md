---
UID: NF:sbtsv.ITsSbTaskPluginNotifySink.OnSetTaskTime
title: ITsSbTaskPluginNotifySink::OnSetTaskTime (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that a task has been scheduled.
helpviewer_keywords: ["ITsSbTaskPluginNotifySink interface [Remote Desktop Services]","OnSetTaskTime method","ITsSbTaskPluginNotifySink.OnSetTaskTime","ITsSbTaskPluginNotifySink::OnSetTaskTime","OnSetTaskTime","OnSetTaskTime method [Remote Desktop Services]","OnSetTaskTime method [Remote Desktop Services]","ITsSbTaskPluginNotifySink interface","sbtsv/ITsSbTaskPluginNotifySink::OnSetTaskTime","termserv.itssbtaskpluginnotifysink_onsettasktime"]
old-location: termserv\itssbtaskpluginnotifysink_onsettasktime.htm
tech.root: TermServ
ms.assetid: 6f9b58ba-8cda-4f8d-9c23-19475262148c
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPluginNotifySink interface [Remote Desktop Services],OnSetTaskTime method, ITsSbTaskPluginNotifySink.OnSetTaskTime, ITsSbTaskPluginNotifySink::OnSetTaskTime, OnSetTaskTime, OnSetTaskTime method [Remote Desktop Services], OnSetTaskTime method [Remote Desktop Services],ITsSbTaskPluginNotifySink interface, sbtsv/ITsSbTaskPluginNotifySink::OnSetTaskTime, termserv.itssbtaskpluginnotifysink_onsettasktime
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbTaskPluginNotifySink::OnSetTaskTime
 - sbtsv/ITsSbTaskPluginNotifySink::OnSetTaskTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbTaskPluginNotifySink.OnSetTaskTime
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

An <a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-rdv_task_status">RDV_TASK_STATUS</a> enumeration value  that represents the state of the task.

### -param saContext [in]

The context bytes associated with the task.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink">ITsSbTaskPluginNotifySink</a>