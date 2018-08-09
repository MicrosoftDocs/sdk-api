---
UID: NF:mstask.IScheduledWorkItem.SetCreator
title: IScheduledWorkItem::SetCreator
author: windows-sdk-content
description: Sets the name of the work item's creator.
old-location: taskschd\ischeduledworkitem_setcreator.htm
old-project: taskschd
ms.assetid: e15c6aba-79f7-407f-81d1-b7ec404c68f9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetCreator method, IScheduledWorkItem.SetCreator, IScheduledWorkItem::SetCreator, SetCreator, SetCreator method [Task Scheduler], SetCreator method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setcreator, mstask/IScheduledWorkItem::SetCreator, taskschd.ischeduledworkitem_setcreator
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
 - IScheduledWorkItem.SetCreator
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::SetCreator


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the name of the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item's</a> creator.


## -parameters




### -param pwszCreator

A null-terminated string that contains the name of the work item's creator.


## -returns



The 
<b>SetCreator</b> method returns one of the following values.

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



Programs must call the <b>IPersistFile::Save</b> method after calling <b>SetCreator</b> to update the creator.




## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/25bbb200-3418-4ca9-87a5-5db537baceee">IScheduledWorkItem::GetCreator</a>
 

 

