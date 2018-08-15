---
UID: NN:taskschd.ITaskSettings3
title: ITaskSettings3
author: windows-sdk-content
description: Provides the extended settings that the Task Scheduler uses to run the task.
old-location: taskschd\itasksettings3.htm
old-project: taskschd
ms.assetid: B0315585-A41C-423C-A059-14C2F04F6652
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITaskSettings3, ITaskSettings3 interface [Task Scheduler], ITaskSettings3 interface [Task Scheduler],described, taskschd.itasksettings3, taskschd/ITaskSettings3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.h
api_name:
 - ITaskSettings3
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskSettings3 interface


## -description


Provides the extended settings that the Task Scheduler uses to run the task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskSettings3</b> interface inherits from <a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>. <b>ITaskSettings3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITaskSettings3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A37F15E-916B-41DD-B168-7F0A7B2E37C3">CreateMantenanceSettings</a>
</td>
<td align="left" width="63%">
Creates a new instance an <a href="https://msdn.microsoft.com/5AB172CA-66BF-47B8-952A-9CBA13A20668">IMaintenanceSettings</a> object and associates it with this <b>ITaskSettings3</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskSettings3</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/F4B6ED81-DE9A-42C8-8F16-D5BD93743CB3">MaintenanceSettings</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a pointer to pointer to an <a href="https://msdn.microsoft.com/5AB172CA-66BF-47B8-952A-9CBA13A20668">IMaintenanceSettings</a>object that Task scheduler uses to perform a task during Automatic maintenance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/C5A28292-13A0-42DC-BF94-4F1A03A3306C">Volatile</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a boolean value that indicates whether the task is automatically disabled every time Windows starts.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>
 

 

