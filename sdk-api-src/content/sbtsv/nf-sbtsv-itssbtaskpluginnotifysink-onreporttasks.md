---
UID: NF:sbtsv.ITsSbTaskPluginNotifySink.OnReportTasks
title: ITsSbTaskPluginNotifySink::OnReportTasks (sbtsv.h)
author: windows-sdk-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) of a new task report.
old-location: termserv\itssbtaskpluginnotifysink_onreporttasks.htm
tech.root: TermServ
ms.assetid: e3b722c2-e6fa-46c5-a851-a039553b8e95
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPluginNotifySink interface [Remote Desktop Services],OnReportTasks method, ITsSbTaskPluginNotifySink.OnReportTasks, ITsSbTaskPluginNotifySink::OnReportTasks, OnReportTasks, OnReportTasks method [Remote Desktop Services], OnReportTasks method [Remote Desktop Services],ITsSbTaskPluginNotifySink interface, sbtsv/ITsSbTaskPluginNotifySink::OnReportTasks, termserv.itssbtaskpluginnotifysink_onreporttasks
ms.topic: method
f1_keywords: 
 - "sbtsv/ITsSbTaskPluginNotifySink.OnReportTasks"
dev_langs:
 - c++
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
 - ITsSbTaskPluginNotifySink.OnReportTasks
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbTaskPluginNotifySink::OnReportTasks


## -description


Notifies Remote Desktop Connection Broker (RD Connection Broker) of a new task report.


## -parameters




### -param szHostName [in]

The name of the host where the report is located.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink">ITsSbTaskPluginNotifySink</a>
 

 

