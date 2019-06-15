---
UID: NN:taskschd.ITaskFolder
title: ITaskFolder (taskschd.h)
author: windows-sdk-content
description: Provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.
old-location: taskschd\itaskfolder.htm
tech.root: taskschd
ms.assetid: da0cc808-b284-4d10-be61-d96c5e07d0a8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITaskFolder, ITaskFolder interface [Task Scheduler], ITaskFolder interface [Task Scheduler],described, taskschd.itaskfolder, taskschd/ITaskFolder
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
 - ITaskFolder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskFolder interface


## -description


Provides the methods that are used to register (create) tasks in the folder, remove tasks from the folder, and create or remove subfolders from the folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskFolder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskFolder</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-createfolder">CreateFolder</a>
</td>
<td align="left" width="63%">
Creates a folder for related tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-deletefolder">DeleteFolder</a>
</td>
<td align="left" width="63%">
Deletes a subfolder from the parent folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-deletetask">DeleteTask</a>
</td>
<td align="left" width="63%">
Deletes a task from the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-getfolder">GetFolder</a>
</td>
<td align="left" width="63%">
Gets a folder that contains tasks at a specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-getfolders">GetFolders</a>
</td>
<td align="left" width="63%">
Gets all the subfolders in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-getsecuritydescriptor">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor for the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettask">GetTask</a>
</td>
<td align="left" width="63%">
Gets a task at a specified location in a folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks">GetTasks</a>
</td>
<td align="left" width="63%">
Gets all the tasks in the folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask">RegisterTask</a>
</td>
<td align="left" width="63%">
Registers (creates) a new task in the folder using XML to define the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">RegisterTaskDefinition</a>
</td>
<td align="left" width="63%">
Registers (creates) a task in a specified location using the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a> interface to define a task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor">SetSecurityDescriptor</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-get_name">Name</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-get_path">Path</a>


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




<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

