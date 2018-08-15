---
UID: NN:sbtsv.ITsSbTaskPluginNotifySink
title: ITsSbTaskPluginNotifySink
author: windows-sdk-content
description: Exposes methods that report status and error messages about tasks to Remote Desktop Connection Broker (RD Connection Broker).
old-location: termserv\itssbtaskpluginnotifysink.htm
old-project: termserv
ms.assetid: dc1b56f3-ea5f-4df5-b90a-ce24c36aee21
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITsSbTaskPluginNotifySink, ITsSbTaskPluginNotifySink interface [Remote Desktop Services], ITsSbTaskPluginNotifySink interface [Remote Desktop Services],described, sbtsv/ITsSbTaskPluginNotifySink, termserv.itssbtaskpluginnotifysink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbtsv.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TS_SB_SORT_BY
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbTaskPluginNotifySink interface


## -description


Exposes methods that report status and error messages about tasks to Remote Desktop Connection Broker (RD Connection Broker).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbTaskPluginNotifySink</b> interface inherits from <a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>. <b>ITsSbTaskPluginNotifySink</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f78a22c3-45e6-4bb1-9ea0-9958339a4ff3">OnDeleteTaskTime</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that a task has been removed from the queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3b722c2-e6fa-46c5-a851-a039553b8e95">OnReportTasks</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker of a new task report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f9b58ba-8cda-4f8d-9c23-19475262148c">OnSetTaskTime</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that a task has been scheduled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fc22173-12b2-41a4-a487-8092088ecfe9">OnUpdateTaskStatus</a>
</td>
<td align="left" width="63%">
Notifies RD Connection Broker that the status of a task has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/11ef1bd4-301f-456b-a68b-2f32b75ac5ae">ITsSbBaseNotifySink</a>



<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

