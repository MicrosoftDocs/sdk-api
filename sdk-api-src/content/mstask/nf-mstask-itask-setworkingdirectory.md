---
UID: NF:mstask.ITask.SetWorkingDirectory
title: ITask::SetWorkingDirectory
author: windows-sdk-content
description: This method sets the working directory for the task.
old-location: taskschd\itask_setworkingdirectory.htm
tech.root: taskschd
ms.assetid: df12d899-c254-4bbf-a49f-d89a2fcb0e28
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ITask interface [Task Scheduler],SetWorkingDirectory method, ITask.SetWorkingDirectory, ITask::SetWorkingDirectory, SetWorkingDirectory, SetWorkingDirectory method [Task Scheduler], SetWorkingDirectory method [Task Scheduler],ITask interface, _msb_itask_setworkingdirectory, mstask/ITask::SetWorkingDirectory, taskschd.itask_setworkingdirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITask.SetWorkingDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# ITask::SetWorkingDirectory


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">working directory</a> for the <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">task</a>.


## -parameters




### -param pwszWorkingDirectory [in]

A null-terminated string that contains a directory path to the working directory for the task. 




The application starts with this directory as the current working directory. To clear the directory, set <i>pwszWorkingDirectory</i> to L"". If the working directory is set to L"", when the application is run, the current directory will be the directory in which the task scheduler service executable, Mstask.exe, resides.


## -returns



The 
<b>SetWorkingDirectory</b> method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available.

</td>
</tr>
</table>
 




## -remarks



After setting the working directory of a task, be sure to call <b>IPersistFile::Save</b> to save the modified task object to disk.


#### Examples

For an example of how to set the working directory of a task, see <a href="https://msdn.microsoft.com/bcfcd6af-a3aa-45a8-bde6-0c90aec3e27a">C/C++ Code Example: Setting Working Directory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/737259f6-63d3-43f1-83a7-a10c95aff0e1">GetWorkingDirectory</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

