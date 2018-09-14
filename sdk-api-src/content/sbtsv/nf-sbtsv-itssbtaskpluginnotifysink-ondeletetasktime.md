---
UID: NF:sbtsv.ITsSbTaskPluginNotifySink.OnDeleteTaskTime
title: ITsSbTaskPluginNotifySink::OnDeleteTaskTime
author: windows-sdk-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that a task has been removed from the queue.
old-location: termserv\itssbtaskpluginnotifysink_ondeletetasktime.htm
tech.root: TermServ
ms.assetid: f78a22c3-45e6-4bb1-9ea0-9958339a4ff3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITsSbTaskPluginNotifySink interface [Remote Desktop Services],OnDeleteTaskTime method, ITsSbTaskPluginNotifySink.OnDeleteTaskTime, ITsSbTaskPluginNotifySink::OnDeleteTaskTime, OnDeleteTaskTime, OnDeleteTaskTime method [Remote Desktop Services], OnDeleteTaskTime method [Remote Desktop Services],ITsSbTaskPluginNotifySink interface, sbtsv/ITsSbTaskPluginNotifySink::OnDeleteTaskTime, termserv.itssbtaskpluginnotifysink_ondeletetasktime
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
 - ITsSbTaskPluginNotifySink.OnDeleteTaskTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbTaskPluginNotifySink::OnDeleteTaskTime


## -description


Notifies Remote Desktop Connection Broker (RD Connection Broker) that a task has been removed from the queue.


## -parameters




### -param szTargetName [in]

The name of the target.


### -param szTaskIdentifier [in]

The GUID that identifies the task.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc1b56f3-ea5f-4df5-b90a-ce24c36aee21">ITsSbTaskPluginNotifySink</a>
 

 

