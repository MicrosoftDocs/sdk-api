---
UID: NF:mstask.IScheduledWorkItem.GetWorkItemData
title: IScheduledWorkItem::GetWorkItemData
author: windows-sdk-content
description: Retrieves application-defined data associated with the work item.
old-location: taskschd\ischeduledworkitem_getworkitemdata.htm
old-project: TaskSchd
ms.assetid: 1b37c412-80ed-44fb-8b3a-b142a9669080
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetWorkItemData, GetWorkItemData method [Task Scheduler], GetWorkItemData method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetWorkItemData method, IScheduledWorkItem.GetWorkItemData, IScheduledWorkItem::GetWorkItemData, _msb_ischeduledworkitem_getworkitemdata, mstask/IScheduledWorkItem::GetWorkItemData, taskschd.ischeduledworkitem_getworkitemdata
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.GetWorkItemData
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::GetWorkItemData


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves application-defined data associated with the <a href="/windows/desktop/api/mstask/ns-mstask-_monthlydow">work item</a>.


## -parameters




### -param pcbData




### -param prgbData






#### - pcBytes [out]

A pointer to the number of bytes copied.


#### - ppBytes [out]

A pointer to a pointer to a BYTE that contains user-defined data for the current work item. The method that invokes 
<b>GetWorkItemData</b> is responsible for freeing this memory by using <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>.


## -returns



The 
<b>GetWorkItemData</b> method returns one of the following values.

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



Retrieving the data of a work item does not affect the operation of the work item in any way.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>



<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/9135b37a-d9f8-4bee-a851-9daca6dc733c">SetWorkItemData</a>
 

 

