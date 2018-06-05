---
UID: NF:mstask.IScheduledWorkItem.GetComment
title: IScheduledWorkItem::GetComment
author: windows-sdk-content
description: Retrieves the comment for the work item.
old-location: taskschd\ischeduledworkitem_getcomment.htm
old-project: TaskSchd
ms.assetid: 49bfd451-8100-40e1-9727-e54c5478b415
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetComment, GetComment method [Task Scheduler], GetComment method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetComment method, IScheduledWorkItem.GetComment, IScheduledWorkItem::GetComment, _msb_ischeduledworkitem_getcomment, mstask/IScheduledWorkItem::GetComment, taskschd.ischeduledworkitem_getcomment
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	IScheduledWorkItem.GetComment
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::GetComment


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the comment for the <a href="w.htm">work item</a>.


## -parameters




### -param ppwszComment [out]

A pointer to a null-terminated string that contains the retrieved comment for the current work item.


## -returns



The 
<b>GetComment</b> method returns one of the following values.

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




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/c6017aa1-8860-454c-a402-becbc1a4ee5c">IScheduledWorkItem::SetComment</a>
 

 

