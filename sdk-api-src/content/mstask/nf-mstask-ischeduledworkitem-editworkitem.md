---
UID: NF:mstask.IScheduledWorkItem.EditWorkItem
title: IScheduledWorkItem::EditWorkItem
author: windows-sdk-content
description: Displays the Task, Schedule, and settings property pages for the work item, allowing a user set the properties on those pages.
old-location: taskschd\ischeduledworkitem_editworkitem.htm
tech.root: TaskSchd
ms.assetid: 3b0b335a-4386-4726-8758-ef5944cb5dfe
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EditWorkItem, EditWorkItem method [Task Scheduler], EditWorkItem method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],EditWorkItem method, IScheduledWorkItem.EditWorkItem, IScheduledWorkItem::EditWorkItem, _msb_ischeduledworkitem_editworkitem, mstask/IScheduledWorkItem::EditWorkItem, taskschd.ischeduledworkitem_editworkitem
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
 - IScheduledWorkItem.EditWorkItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# IScheduledWorkItem::EditWorkItem


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Displays the Task, Schedule, and settings property pages for the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a>, allowing a user set the properties on those pages.


## -parameters




### -param hParent [in]

Reserved for future use. Set this parameter to <b>NULL</b>.


### -param dwReserved [in]

Reserved for internal use; this parameter must be set to zero.


## -returns



The 
<b>EditWorkItem</b> method returns one of the following values.

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
<dt><b>STG_E_NOTFILEBASEDSTORAGE</b></dt>
</dl>
</td>
<td width="60%">
The work item object is not persistent.

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
 

 

