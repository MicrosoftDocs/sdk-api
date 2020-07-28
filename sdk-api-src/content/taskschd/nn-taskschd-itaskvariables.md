---
UID: NN:taskschd.ITaskVariables
title: ITaskVariables (taskschd.h)
description: Defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.
helpviewer_keywords: ["ITaskVariables","ITaskVariables interface [Task Scheduler]","ITaskVariables interface [Task Scheduler]","described","taskschd.itaskvariables","taskschd/ITaskVariables"]
old-location: taskschd\itaskvariables.htm
tech.root: taskschd
ms.assetid: 4f7a9dd3-0bf4-4c23-acdb-a5e0389120cc
ms.date: 12/05/2018
ms.keywords: ITaskVariables, ITaskVariables interface [Task Scheduler], ITaskVariables interface [Task Scheduler],described, taskschd.itaskvariables, taskschd/ITaskVariables
f1_keywords:
- taskschd/ITaskVariables
dev_langs:
- c++
req.header: taskschd.h
req.include-header: 
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- ITaskVariables
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskVariables interface


## -description


Defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks. Task handlers that need to input and output data to job variables should do a query interface on the services pointer for <b>ITaskVariables</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskVariables</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskVariables</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskvariables-getcontext">GetContext</a>
</td>
<td align="left" width="63%">
Used to share the context between different steps and tasks that are in the same job instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskvariables-getinput">GetInput</a>
</td>
<td align="left" width="63%">
Gets the input variables for a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskvariables-setoutput">SetOutput</a>
</td>
<td align="left" width="63%">
Sets the output variables for a task.

</td>
</tr>
</table> 

