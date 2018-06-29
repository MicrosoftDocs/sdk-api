---
UID: NF:mstask.IScheduledWorkItem.GetAccountInformation
title: IScheduledWorkItem::GetAccountInformation
author: windows-sdk-content
description: Retrieves the account name for the work item.
old-location: taskschd\ischeduledworkitem_getaccountinformation.htm
old-project: TaskSchd
ms.assetid: d5f279ac-bf03-4af5-9bad-58eadaba0ca1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetAccountInformation, GetAccountInformation method [Task Scheduler], GetAccountInformation method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetAccountInformation method, IScheduledWorkItem.GetAccountInformation, IScheduledWorkItem::GetAccountInformation, _msb_ischeduledworkitem_getaccountinformation, mstask/IScheduledWorkItem::GetAccountInformation, taskschd.ischeduledworkitem_getaccountinformation
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
 - IScheduledWorkItem.GetAccountInformation
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IScheduledWorkItem::GetAccountInformation


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the account name for the <a href="https://msdn.microsoft.com/library/Aa381060(v=VS.85).aspx">work item</a>.


## -parameters




### -param ppwszAccountName [out]

A pointer to a null-terminated string that contains the account name for the current work item. The empty string, L"", is returned for the local system account. 




After processing the account name, be sure to call <b>CoTaskMemFree</b> to free the string.


## -returns



The 
<b>GetAccountInformation</b> method returns one of the following values.

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
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_ACCOUNT_INFORMATION_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The account information has not been set for the work item.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_NO_SECURITY_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
Security services are available only on the Windows Server 2003, Windows 2000, and Windows XP operating systems.

</td>
</tr>
</table>
 




## -remarks



The 
<b>GetAccountInformation</b> method is for the Windows Server 2003, Windows XP, and Windows 2000 operating systems.


#### Examples

For more information and an example of how to retrieve the account information of a task, see <a href="https://msdn.microsoft.com/ef330276-a063-42c6-a837-fddb4723091b">C/C++ Code Example: Retrieving Task Account Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/fae1299f-2f3f-48cf-91d9-1057ce62172b">IScheduledWorkItem::SetAccountInformation</a>
 

 

