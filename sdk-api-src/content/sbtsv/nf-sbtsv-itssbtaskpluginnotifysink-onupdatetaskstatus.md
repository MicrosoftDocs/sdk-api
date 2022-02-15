---
UID: NF:sbtsv.ITsSbTaskPluginNotifySink.OnUpdateTaskStatus
title: ITsSbTaskPluginNotifySink::OnUpdateTaskStatus (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of a task has changed.
helpviewer_keywords: ["ITsSbTaskPluginNotifySink interface [Remote Desktop Services]","OnUpdateTaskStatus method","ITsSbTaskPluginNotifySink.OnUpdateTaskStatus","ITsSbTaskPluginNotifySink::OnUpdateTaskStatus","OnUpdateTaskStatus","OnUpdateTaskStatus method [Remote Desktop Services]","OnUpdateTaskStatus method [Remote Desktop Services]","ITsSbTaskPluginNotifySink interface","sbtsv/ITsSbTaskPluginNotifySink::OnUpdateTaskStatus","termserv.itssbtaskpluginnotifysink_onupdatetaskstatus"]
old-location: termserv\itssbtaskpluginnotifysink_onupdatetaskstatus.htm
tech.root: TermServ
ms.assetid: 5fc22173-12b2-41a4-a487-8092088ecfe9
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPluginNotifySink interface [Remote Desktop Services],OnUpdateTaskStatus method, ITsSbTaskPluginNotifySink.OnUpdateTaskStatus, ITsSbTaskPluginNotifySink::OnUpdateTaskStatus, OnUpdateTaskStatus, OnUpdateTaskStatus method [Remote Desktop Services], OnUpdateTaskStatus method [Remote Desktop Services],ITsSbTaskPluginNotifySink interface, sbtsv/ITsSbTaskPluginNotifySink::OnUpdateTaskStatus, termserv.itssbtaskpluginnotifysink_onupdatetaskstatus
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
 - ITsSbTaskPluginNotifySink::OnUpdateTaskStatus
 - sbtsv/ITsSbTaskPluginNotifySink::OnUpdateTaskStatus
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
 - ITsSbTaskPluginNotifySink.OnUpdateTaskStatus
---

# ITsSbTaskPluginNotifySink::OnUpdateTaskStatus


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of a task has changed.

## -parameters

### -param szTargetName [in]

The name of the target.

### -param TaskIdentifier [in]

The GUID that identifies the task.

### -param TaskStatus [in]

An <a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-rdv_task_status">RDV_TASK_STATUS</a> enumeration value representing the new state of the task.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink">ITsSbTaskPluginNotifySink</a>