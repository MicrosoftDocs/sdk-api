---
UID: NF:mstask.IScheduledWorkItem.GetCreator
title: IScheduledWorkItem::GetCreator
author: windows-sdk-content
description: Retrieves the name of the creator of the work item.
old-location: taskschd\ischeduledworkitem_getcreator.htm
tech.root: TaskSchd
ms.assetid: 25bbb200-3418-4ca9-87a5-5db537baceee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCreator, GetCreator method [Task Scheduler], GetCreator method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetCreator method, IScheduledWorkItem.GetCreator, IScheduledWorkItem::GetCreator, _msb_ischeduledworkitem_getcreator, mstask/IScheduledWorkItem::GetCreator, taskschd.ischeduledworkitem_getcreator
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
 - IScheduledWorkItem.GetCreator
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# IScheduledWorkItem::GetCreator


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the name of the creator of the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a>.


## -parameters




### -param ppwszCreator [out]

A pointer to a null-terminated string that contains the name of the creator of the current work item. The application that invokes 
<b>GetCreator</b> is responsible for freeing this string using the <b>CoTaskMemFree</b> function.


## -returns



The 
<b>GetCreator</b> method returns one of the following values.

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



<a href="https://msdn.microsoft.com/e15c6aba-79f7-407f-81d1-b7ec404c68f9">IScheduledWorkItem::SetCreator</a>
 

 

