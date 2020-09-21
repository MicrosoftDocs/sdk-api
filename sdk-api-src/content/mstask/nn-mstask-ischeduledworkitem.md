---
UID: NN:mstask.IScheduledWorkItem
title: IScheduledWorkItem (mstask.h)
description: Provides the methods for managing specific work items.
helpviewer_keywords: ["IScheduledWorkItem","IScheduledWorkItem interface [Task Scheduler]","IScheduledWorkItem interface [Task Scheduler]","described","_msb_ischeduledworkitem","mstask/IScheduledWorkItem","taskschd.ischeduledworkitem"]
old-location: taskschd\ischeduledworkitem.htm
tech.root: taskschd
ms.assetid: e668833a-094d-4504-90a0-87912a6a53c2
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem, IScheduledWorkItem interface [Task Scheduler], IScheduledWorkItem interface [Task Scheduler],described, _msb_ischeduledworkitem, mstask/IScheduledWorkItem, taskschd.ischeduledworkitem
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
 - IScheduledWorkItem
 - mstask/IScheduledWorkItem
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
 - IScheduledWorkItem
---

# IScheduledWorkItem interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for managing specific <a href="/windows/desktop/TaskSchd/w">work items</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IScheduledWorkItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IScheduledWorkItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IScheduledWorkItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-createtrigger">CreateTrigger</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/TaskSchd/t">trigger</a> using a work item object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-deletetrigger">DeleteTrigger</a>
</td>
<td align="left" width="63%">
Deletes a trigger from a work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-editworkitem">EditWorkItem</a>
</td>
<td align="left" width="63%">
Opens the configuration properties for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getaccountinformation">GetAccountInformation</a>
</td>
<td align="left" width="63%">
Retrieves the account name for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getcomment">GetComment</a>
</td>
<td align="left" width="63%">
Retrieves the comment for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getcreator">GetCreator</a>
</td>
<td align="left" width="63%">
Retrieves the creator of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-geterrorretrycount">GetErrorRetryCount</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-geterrorretryinterval">GetErrorRetryInterval</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getexitcode">GetExitCode</a>
</td>
<td align="left" width="63%">
Retrieves the work item's last exit code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getflags">GetFlags</a>
</td>
<td align="left" width="63%">
Retrieves the flags that modify the behavior of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getidlewait">GetIdleWait</a>
</td>
<td align="left" width="63%">
Retrieves the idle wait time for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getmostrecentruntime">GetMostRecentRunTime</a>
</td>
<td align="left" width="63%">
Retrieves the most recent time the work item began running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getnextruntime">GetNextRunTime</a>
</td>
<td align="left" width="63%">
Retrieves the next time the work item will run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getruntimes">GetRunTimes</a>
</td>
<td align="left" width="63%">
Retrieves the work item run times for a specified time period.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getstatus">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettrigger">GetTrigger</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="/windows/desktop/TaskSchd/t">trigger structure</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettriggercount">GetTriggerCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of triggers associated with a work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettriggerstring">GetTriggerString</a>
</td>
<td align="left" width="63%">
Retrieves a <a href="/windows/desktop/TaskSchd/t">trigger string</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getworkitemdata">GetWorkItemData</a>
</td>
<td align="left" width="63%">
Retrieves application-defined data associated with the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-run">Run</a>
</td>
<td align="left" width="63%">
Runs the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setaccountinformation">SetAccountInformation</a>
</td>
<td align="left" width="63%">
Sets the account name and password for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setcomment">SetComment</a>
</td>
<td align="left" width="63%">
Sets the comment for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setcreator">SetCreator</a>
</td>
<td align="left" width="63%">
Sets the creator of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-seterrorretrycount">SetErrorRetryCount</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-seterrorretryinterval">SetErrorRetryInterval</a>
</td>
<td align="left" width="63%">
Not currently implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">SetFlags</a>
</td>
<td align="left" width="63%">
Sets the flags that modify the behavior of the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setidlewait">SetIdleWait</a>
</td>
<td align="left" width="63%">
Sets the <a href="/windows/desktop/TaskSchd/i">idle wait time</a> for the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setworkitemdata">SetWorkItemData</a>
</td>
<td align="left" width="63%">
Stores application-defined data associated with the work item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-terminate">Terminate</a>
</td>
<td align="left" width="63%">
Ends the execution of the work item.

</td>
</tr>
</table>

## -remarks

The <b>IScheduledWorkItem</b> interface is the base interface for the 
<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a> interface. All methods provided by 
<b>IScheduledWorkItem</b> are inherited by the 
<b>ITask</b> interface and are typically called through that interface.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/c-c-code-example-terminating-a-task">C/C++ Code Example: Terminating a Task</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>