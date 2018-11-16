---
UID: NF:mstask.IScheduledWorkItem.CreateTrigger
title: IScheduledWorkItem::CreateTrigger
author: windows-sdk-content
description: Creates a trigger for the work item.
old-location: taskschd\ischeduledworkitem_createtrigger.htm
tech.root: TaskSchd
ms.assetid: ff8c9c3b-697f-42f0-a5b5-6194e4c89096
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateTrigger, CreateTrigger method [Task Scheduler], CreateTrigger method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],CreateTrigger method, IScheduledWorkItem.CreateTrigger, IScheduledWorkItem::CreateTrigger, _msb_ischeduledworkitem_createtrigger, mstask/IScheduledWorkItem::CreateTrigger, taskschd.ischeduledworkitem_createtrigger
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
 - IScheduledWorkItem.CreateTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
- apiref
: 
- COM
: 
- mstask.h
: 
- IScheduledWorkItem.CreateTrigger
: 
---

# IScheduledWorkItem::CreateTrigger


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Creates a trigger for the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a>.


## -parameters




### -param piNewTrigger [out]

A pointer to the returned trigger index value of the new trigger. The trigger index for the first trigger associated with a work item is "0". See Remarks for other uses of the trigger index.


### -param ppTrigger [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/990702f4-fb6f-47a7-b538-f6632f831a4e">ITaskTrigger</a> interface. Currently, the only supported work items are <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">tasks</a>.


## -returns



The 
<b>CreateTrigger</b> method returns one of the following values.

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



You use the trigger index returned by <i>piNewTrigger</i> when you are either retrieving or  deleting triggers. However, the trigger index is not an identifier. It indicates only the new trigger's position relative to the other current triggers associated with the work item.

To set the criteria for the new trigger, call 
<a href="https://msdn.microsoft.com/2f445835-a409-4a03-b853-4e0b07ded1ea">ITaskTrigger::SetTrigger</a>.

After creating a new trigger for a work item, applications must call the 
<a href="https://msdn.microsoft.com/en-us/library/ms693701(v=VS.85).aspx">IPersistFile::Save</a> method to save the new trigger to disk.


#### Examples

For an example of how to set the trigger criteria when creating a new trigger, see <a href="https://msdn.microsoft.com/c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5">Creating a New Trigger</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693701(v=VS.85).aspx">IPersistFile::Save</a>



<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/418e16d3-67ee-4b77-a7a9-67e722619d80">IScheduledWorkItem::DeleteTrigger</a>



<a href="https://msdn.microsoft.com/f99b342c-9233-43e3-93f1-88586e975608">IScheduledWorkItem::GetTrigger</a>



<a href="https://msdn.microsoft.com/5e342807-4796-449b-b490-815ce57f4d8f">IScheduledWorkItem::GetTriggerString</a>



<a href="https://msdn.microsoft.com/990702f4-fb6f-47a7-b538-f6632f831a4e">ITaskTrigger</a>



<a href="https://msdn.microsoft.com/2f445835-a409-4a03-b853-4e0b07ded1ea">ITaskTrigger::SetTrigger</a>
 

 

