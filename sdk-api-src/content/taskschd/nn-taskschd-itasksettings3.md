---
UID: NN:taskschd.ITaskSettings3
title: ITaskSettings3 (taskschd.h)
author: windows-sdk-content
description: Provides the extended settings that the Task Scheduler uses to run the task.
old-location: taskschd\itasksettings3.htm
tech.root: taskschd
ms.assetid: B0315585-A41C-423C-A059-14C2F04F6652
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskSettings3, ITaskSettings3 interface [Task Scheduler], ITaskSettings3 interface [Task Scheduler],described, taskschd.itasksettings3, taskschd/ITaskSettings3
ms.topic: interface
f1_keywords: 
 - "taskschd/ITaskSettings3"
dev_langs:
 - c++
req.header: taskschd.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.h
api_name:
 - ITaskSettings3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskSettings3 interface


## -description


Provides the extended settings that the Task Scheduler uses to run the task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskSettings3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>. <b>ITaskSettings3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh832149(v=vs.85)">CreateMantenanceSettings</a>
</td>
<td align="left" width="63%">
Creates a new instance an <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-imaintenancesettings">IMaintenanceSettings</a> object and associates it with this <b>ITaskSettings3</b> object.

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

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings3-get_maintenancesettings">MaintenanceSettings</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a pointer to pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-imaintenancesettings">IMaintenanceSettings</a>object that Task scheduler uses to perform a task during Automatic maintenance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itasksettings3-get_volatile">Volatile</a>


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




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>
 

 

