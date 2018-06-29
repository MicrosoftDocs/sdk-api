---
UID: NF:mstask.IScheduledWorkItem.SetWorkItemData
title: IScheduledWorkItem::SetWorkItemData
author: windows-sdk-content
description: This method stores application-defined data associated with the work item.
old-location: taskschd\ischeduledworkitem_setworkitemdata.htm
old-project: TaskSchd
ms.assetid: 9135b37a-d9f8-4bee-a851-9daca6dc733c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetWorkItemData method, IScheduledWorkItem.SetWorkItemData, IScheduledWorkItem::SetWorkItemData, SetWorkItemData, SetWorkItemData method [Task Scheduler], SetWorkItemData method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setworkitemdata, mstask/IScheduledWorkItem::SetWorkItemData, taskschd.ischeduledworkitem_setworkitemdata
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
 - IScheduledWorkItem.SetWorkItemData
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::SetWorkItemData


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method stores application-defined data associated with the <a href="https://msdn.microsoft.com/library/Aa381060(v=VS.85).aspx">work item</a>.


## -parameters




### -param cbData




### -param rgbData [in]

The data to copy.


#### - cBytes [in]

The number of bytes in the data buffer. The caller allocates and frees this memory.


## -returns



The 
<b>SetWorkItemData</b> method returns one of the following values.

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



You can retrieve data by calling 
<a href="https://msdn.microsoft.com/1b37c412-80ed-44fb-8b3a-b142a9669080">IScheduledWorkItem::GetWorkItemData</a>.

Programs must call the <b>IPersistFile::Save</b> method after calling 
<b>SetWorkItemData</b> to update the work item data.




## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/1b37c412-80ed-44fb-8b3a-b142a9669080">IScheduledWorkItem::GetWorkItemData</a>
 

 

