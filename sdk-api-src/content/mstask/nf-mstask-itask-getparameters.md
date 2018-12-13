---
UID: NF:mstask.ITask.GetParameters
title: ITask::GetParameters
author: windows-sdk-content
description: This method retrieves the task's command-line parameters.
old-location: taskschd\itask_getparameters.htm
tech.root: taskschd
ms.assetid: f59118d6-b430-4fcd-9c78-e6b5a65c151a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetParameters, GetParameters method [Task Scheduler], GetParameters method [Task Scheduler],ITask interface, ITask interface [Task Scheduler],GetParameters method, ITask.GetParameters, ITask::GetParameters, _msb_itask_getparameters, mstask/ITask::GetParameters, taskschd.itask_getparameters
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
 - ITask.GetParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# ITask::GetParameters


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">task's</a> command-line parameters.


## -parameters




### -param ppwszParameters [out]

A pointer to a null-terminated string that contains the command-line parameters for the task. The method that invokes 
<b>GetParameters</b> is responsible for freeing this string using the <b>CoTaskMemFree</b> function.


## -returns



The 
<b>GetParameters</b> method returns one of the following values.

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
 




## -see-also




<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>



<a href="https://msdn.microsoft.com/094dcd8f-35aa-4300-b58d-c846bca1c88c">SetParameters</a>
 

 

