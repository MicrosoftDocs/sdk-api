---
UID: NN:taskschd.ITaskFolder
title: ITaskFolder
author: windows-driver-content
description: Provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.
old-location: taskschd\itaskfolder.htm
old-project: TaskSchd
ms.assetid: da0cc808-b284-4d10-be61-d96c5e07d0a8
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITaskFolder, ITaskFolder interface [Task Scheduler], ITaskFolder interface [Task Scheduler],described, taskschd.itaskfolder, taskschd/ITaskFolder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskFolder
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskFolder interface


## -description


Provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskFolder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskFolder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITaskFolder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da0f2420-b1a0-4359-aa05-ddf1f2a35118">CreateFolder</a>
</td>
<td align="left" width="63%">
Creates a folder for related tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7758afc5-73d8-456c-98a9-89e4b7ad42b9">DeleteFolder</a>
</td>
<td align="left" width="63%">
Deletes a subfolder from the parent folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b929abd-c40a-4f6b-9a0b-702d2f26f1fe">DeleteTask</a>
</td>
<td align="left" width="63%">
Deletes a task from the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62a0b946-ba06-46cf-bf38-e6774bdaae0a">GetFolder</a>
</td>
<td align="left" width="63%">
Gets a folder that contains tasks at a specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee00a8be-52f5-4399-9a1f-18e06121a3da">GetFolders</a>
</td>
<td align="left" width="63%">
Gets all the subfolders in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9360746e-0f6d-40cb-9135-b12bd8b7d760">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor for the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01c32103-d65a-49ed-b12e-af2e865456e1">GetTask</a>
</td>
<td align="left" width="63%">
Gets a task at a specified location in a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2dcef962-d4b0-4fc9-845a-e33f020dba41">GetTasks</a>
</td>
<td align="left" width="63%">
Gets all the tasks in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/743e5bd9-3fb6-4e09-96ed-ca2d74fa0bab">RegisterTask</a>
</td>
<td align="left" width="63%">
Registers (creates) a new task in the folder using XML to define the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">RegisterTaskDefinition</a>
</td>
<td align="left" width="63%">
Registers (creates) a task in a specified location using the <a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a> interface to define a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54f8a37b-87ac-449c-8e03-aeacd27e8c97">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor for the folder.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskFolder</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name that is used to identify the folder that contains a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915708">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the path to where the folder is stored.

</td>
</tr>
</table> 


## -see-also




<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

