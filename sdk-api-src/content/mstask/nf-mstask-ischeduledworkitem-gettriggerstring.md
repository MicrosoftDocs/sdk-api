---
UID: NF:mstask.IScheduledWorkItem.GetTriggerString
title: IScheduledWorkItem::GetTriggerString (mstask.h)
description: Retrieves a string that describes the work item trigger.
helpviewer_keywords: ["GetTriggerString","GetTriggerString method [Task Scheduler]","GetTriggerString method [Task Scheduler]","IScheduledWorkItem interface","IScheduledWorkItem interface [Task Scheduler]","GetTriggerString method","IScheduledWorkItem.GetTriggerString","IScheduledWorkItem::GetTriggerString","_msb_ischeduledworkitem_gettriggerstring","mstask/IScheduledWorkItem::GetTriggerString","taskschd.ischeduledworkitem_gettriggerstring"]
old-location: taskschd\ischeduledworkitem_gettriggerstring.htm
tech.root: taskschd
ms.assetid: 5e342807-4796-449b-b490-815ce57f4d8f
ms.date: 12/05/2018
ms.keywords: GetTriggerString, GetTriggerString method [Task Scheduler], GetTriggerString method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetTriggerString method, IScheduledWorkItem.GetTriggerString, IScheduledWorkItem::GetTriggerString, _msb_ischeduledworkitem_gettriggerstring, mstask/IScheduledWorkItem::GetTriggerString, taskschd.ischeduledworkitem_gettriggerstring
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
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - IScheduledWorkItem::GetTriggerString
 - mstask/IScheduledWorkItem::GetTriggerString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.GetTriggerString
---

# IScheduledWorkItem::GetTriggerString


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

 Retrieves a string that describes the <a href="/windows/desktop/TaskSchd/w">work item</a> trigger.

## -parameters

### -param iTrigger [in]

The index of the trigger to be retrieved. The first trigger is always referenced by 0. For more information, see Remarks.

### -param ppwszTrigger [out]

A pointer to a null-terminated string that contains the retrieved trigger description. Note that this string must be release by a call to <b>CoTaskMemFree</b> after the string is no longer needed.

## -returns

The 
<b>GetTriggerString</b> method returns one of the following values.

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

A trigger index is not an identifier. It only indicates the trigger's position relative to the current triggers associated with the work item. For example, if you create four triggers, they will be numbered 0 through 3. But if the second trigger is deleted, the remaining triggers will be numbered 0 through 2. Note that the index of the first trigger is always 0, and the index of the last trigger is one less than the total number of triggers for the work item (TriggerCount -1).

You can retrieve the trigger count using 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettriggercount">IScheduledWorkItem::GetTriggerCount</a>.


#### Examples

For an example of how to retrieve the trigger string of all triggers associated with a task, see <a href="/windows/desktop/TaskSchd/retrieving-trigger-strings-example">Retrieving Trigger Strings Example</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>