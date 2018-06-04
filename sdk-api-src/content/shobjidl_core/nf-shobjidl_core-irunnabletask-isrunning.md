---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRunnableTask::IsRunning


## -description


Requests information on the state of a task, such as thumbnail extraction.


## -parameters






## -returns



Type: <b>LONG</b>

Returns one of the following values to indicate the current execution state.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
Extraction has not yet started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The task is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_SUSPENDED</b></dt>
</dl>
</td>
<td width="60%">
The task is suspended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_PENDING</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/7465aded-43ff-4b63-8a90-b9f55240625b">IRunnableTask::Kill</a> has been called on the thread, but the thread has not yet completely shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_FINISHED</b></dt>
</dl>
</td>
<td width="60%">
The task is finished.

</td>
</tr>
</table>
 




## -remarks



This method must be implemented.



