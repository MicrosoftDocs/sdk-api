---
UID: NF:mstask.IScheduledWorkItem.SetComment
title: IScheduledWorkItem::SetComment
author: windows-sdk-content
description: Sets the comment for the work item.
old-location: taskschd\ischeduledworkitem_setcomment.htm
tech.root: taskschd
ms.assetid: c6017aa1-8860-454c-a402-becbc1a4ee5c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetComment method, IScheduledWorkItem.SetComment, IScheduledWorkItem::SetComment, SetComment, SetComment method [Task Scheduler], SetComment method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setcomment, mstask/IScheduledWorkItem::SetComment, taskschd.ischeduledworkitem_setcomment
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
 - IScheduledWorkItem.SetComment
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# IScheduledWorkItem::SetComment


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the comment for the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a>.


## -parameters




### -param pwszComment [in]

A null-terminated string that specifies the comment for the current work item.


## -returns



The 
<b>SetComment</b> method returns one of the following values.

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



After setting the comment of a work item, be sure to call <b>IPersistFile::Save</b> to save the modified work item object to disk.


#### Examples

For an example of how to set the comment of a task, see <a href="https://msdn.microsoft.com/c91da741-07fe-41fb-94d5-f6a45ef2d89d">C/C++ Code Example: Setting Task Comment</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/49bfd451-8100-40e1-9727-e54c5478b415">IScheduledWorkItem::GetComment</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

