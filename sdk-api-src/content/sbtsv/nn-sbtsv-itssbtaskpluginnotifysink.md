---
UID: NN:sbtsv.ITsSbTaskPluginNotifySink
title: ITsSbTaskPluginNotifySink (sbtsv.h)
author: windows-sdk-content
description: Exposes methods that report status and error messages about tasks to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbtaskpluginnotifysink.htm
tech.root: TermServ
ms.assetid: dc1b56f3-ea5f-4df5-b90a-ce24c36aee21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbTaskPluginNotifySink, ITsSbTaskPluginNotifySink interface [Remote Desktop Services], ITsSbTaskPluginNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbTaskPluginNotifySink, termserv.itssbtaskpluginnotifysink
ms.topic: interface
f1_keywords: ["sbtsv/ITsSbTaskPluginNotifySink"]
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
 - ITsSbTaskPluginNotifySink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbTaskPluginNotifySink interface


## -description


Exposes methods that report status and error messages about tasks to Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbTaskPluginNotifySink</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>. <b>ITsSbTaskPluginNotifySink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbTaskPluginNotifySink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-ondeletetasktime">OnDeleteTaskTime</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that a task has been removed from the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-onreporttasks">OnReportTasks</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker of a new task report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-onsettasktime">OnSetTaskTime</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that a task has been scheduled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-onupdatetaskstatus">OnUpdateTaskStatus</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the status of a task has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink">ITsSbBaseNotifySink</a>



<a href="https://docs.microsoft.com/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>
 

 

