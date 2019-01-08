---
UID: NF:sbtsv.ITsSbTaskPluginNotifySink.OnUpdateTaskStatus
title: ITsSbTaskPluginNotifySink::OnUpdateTaskStatus
author: windows-sdk-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of a task has changed.
old-location: termserv\itssbtaskpluginnotifysink_onupdatetaskstatus.htm
tech.root: termserv
ms.assetid: 5fc22173-12b2-41a4-a487-8092088ecfe9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITsSbTaskPluginNotifySink interface [Remote Desktop Services],OnUpdateTaskStatus method, ITsSbTaskPluginNotifySink.OnUpdateTaskStatus, ITsSbTaskPluginNotifySink::OnUpdateTaskStatus, OnUpdateTaskStatus, OnUpdateTaskStatus method [Remote Desktop Services], OnUpdateTaskStatus method [Remote Desktop Services],ITsSbTaskPluginNotifySink interface, sbtsv/ITsSbTaskPluginNotifySink::OnUpdateTaskStatus, termserv.itssbtaskpluginnotifysink_onupdatetaskstatus
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbTaskPluginNotifySink.OnUpdateTaskStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

An <a href="https://msdn.microsoft.com/69278A29-9100-4855-B5B3-C790563B8B72">RDV_TASK_STATUS</a> enumeration value representing the new state of the task.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc1b56f3-ea5f-4df5-b90a-ce24c36aee21">ITsSbTaskPluginNotifySink</a>
 

 

