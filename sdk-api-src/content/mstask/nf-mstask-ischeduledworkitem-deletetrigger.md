---
UID: NF:mstask.IScheduledWorkItem.DeleteTrigger
title: IScheduledWorkItem::DeleteTrigger
author: windows-sdk-content
description: Deletes a trigger from a work item.
old-location: taskschd\ischeduledworkitem_deletetrigger.htm
tech.root: TaskSchd
ms.assetid: 418e16d3-67ee-4b77-a7a9-67e722619d80
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DeleteTrigger, DeleteTrigger method [Task Scheduler], DeleteTrigger method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],DeleteTrigger method, IScheduledWorkItem.DeleteTrigger, IScheduledWorkItem::DeleteTrigger, _msb_ischeduledworkitem_deletetrigger, mstask/IScheduledWorkItem::DeleteTrigger, taskschd.ischeduledworkitem_deletetrigger
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
 - IScheduledWorkItem.DeleteTrigger
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# IScheduledWorkItem::DeleteTrigger


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Deletes a trigger from a <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a>.


## -parameters




### -param iTrigger [in]

A trigger index value that specifies the trigger to be deleted. For more information, see Remarks.


## -returns



The 
<b>DeleteTrigger</b> method returns one of the following values.

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



A trigger index is created for each trigger when the trigger is created. However, it is not a unique identifier for a specific trigger. For example, if you create four triggers, they will be numbered 0 through 3. But if the second trigger is deleted, the remaining triggers will be numbered 0 through 2. Note that the index of the first trigger is always 0, and the index of the last trigger is one less than the total number of triggers for the work item (TriggerCount -1).

You can retrieve the trigger count using 
<a href="https://msdn.microsoft.com/db1c98db-c4c1-45af-baba-097ee8dc6abf">IScheduledWorkItem::GetTriggerCount</a>.

To complete the deletion of the trigger, programs must call the <b>IPersistFile::Save</b> method after calling 
<b>DeleteTrigger</b>. Calling <b>IPersistFile::Save</b> saves the changes to disk.




## -see-also




<a href="https://msdn.microsoft.com/ff8c9c3b-697f-42f0-a5b5-6194e4c89096">CreateTrigger</a>



<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/db1c98db-c4c1-45af-baba-097ee8dc6abf">IScheduledWorkItem::GetTriggerCount</a>
 

 

