---
UID: NN:taskschd.ITaskVariables
title: ITaskVariables
author: windows-sdk-content
description: Defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.
old-location: taskschd\itaskvariables.htm
old-project: taskschd
ms.assetid: 4f7a9dd3-0bf4-4c23-acdb-a5e0389120cc
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITaskVariables, ITaskVariables interface [Task Scheduler], ITaskVariables interface [Task Scheduler],described, taskschd.itaskvariables, taskschd/ITaskVariables
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: taskschd.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - taskschd.dll
api_name:
 - ITaskVariables
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskVariables interface


## -description


Defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks. Task handlers that need to input and output data to job variables should do a query interface on the services pointer for <b>ITaskVariables</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskVariables</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskVariables</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskVariables</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/090d24ac-18eb-4a76-887f-30d3b99e7ad0">GetContext</a>
</td>
<td align="left" width="63%">
Used to share the context between different steps and tasks that are in the same job instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c38a633-b3f1-4894-9152-e01a083a54fc">GetInput</a>
</td>
<td align="left" width="63%">
Gets the input variables for a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/989e61c8-f15e-42c6-ab90-c00cc90eb464">SetOutput</a>
</td>
<td align="left" width="63%">
Sets the output variables for a task.

</td>
</tr>
</table> 

