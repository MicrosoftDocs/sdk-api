---
UID: NF:mstask.IScheduledWorkItem.SetAccountInformation
title: IScheduledWorkItem::SetAccountInformation (mstask.h)
description: Sets the account name and password used to run the work item.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetAccountInformation method","IScheduledWorkItem.SetAccountInformation","IScheduledWorkItem::SetAccountInformation","SetAccountInformation","SetAccountInformation method [Task Scheduler]","SetAccountInformation method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_setaccountinformation","mstask/IScheduledWorkItem::SetAccountInformation","taskschd.ischeduledworkitem_setaccountinformation"]
old-location: taskschd\ischeduledworkitem_setaccountinformation.htm
tech.root: taskschd
ms.assetid: fae1299f-2f3f-48cf-91d9-1057ce62172b
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetAccountInformation method, IScheduledWorkItem.SetAccountInformation, IScheduledWorkItem::SetAccountInformation, SetAccountInformation, SetAccountInformation method [Task Scheduler], SetAccountInformation method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setaccountinformation, mstask/IScheduledWorkItem::SetAccountInformation, taskschd.ischeduledworkitem_setaccountinformation
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IScheduledWorkItem::SetAccountInformation
 - mstask/IScheduledWorkItem::SetAccountInformation
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
 - IScheduledWorkItem.SetAccountInformation
---

# IScheduledWorkItem::SetAccountInformation


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the account name and password used to run the <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param pwszAccountName [in]

A string that contains the <b>null</b>-terminated name of the user account in which the work item will run. To specify the local system account, use the empty string, L"". Do not use any other string to specify the local system account. For more information, see Remarks.

### -param pwszPassword [in]

A string that contains the password for the account specified in <i>pwszAccountName</i>. 




Set this parameter to <b>NULL</b> if the local system account is specified. If you set the TASK_FLAG_RUN_ONLY_IF_LOGGED_ON flag, you may also set <i>pwszPassword</i> to <b>NULL</b> for local or domain user accounts. Use the <a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a> method to set the flag.

Task Scheduler stores account information only once for all tasks that use the same account. If the account password is updated for one task, then all tasks using that same account will use the updated password.

When you have finished using the password, clear the password information by calling the <a href="/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)">SecureZeroMemory</a> function. For more information about protecting passwords, see <a href="/windows/desktop/SecBP/handling-passwords">Handling Passwords</a>.

## -returns

The 
<b>SetAccountInformation</b> method returns one of the following values. Note that errors from this call may also be returned by the subsequent call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a>.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to perform the operation. For more information, see Remarks.

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
<dt><b>SCHED_E_NO_SECURITY_SERVICES</b></dt>
</dl>
</td>
<td width="60%">
Security services are available only on the Windows Server 2003, Windows XP, and Windows 2000.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_UNSUPPORTED_ACCOUNT_OPTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszPassword</i> parameter was set to <b>NULL</b>, but the TASK_FLAG_RUN_ONLY_IF_LOGGED_ON flag was not set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> SCHED_E_ACCOUNT_INFORMATION_NOT_SET </b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszPassword</i> parameter was incorrect.  In the Windows Server 2003, Task Scheduler validates the password at the time the job is created (during a call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a>). Be aware that if this error occurs, the job file will still be created.

</td>
</tr>
</table>

## -remarks

This method is for the Windows Server 2003, Windows XP, and Windows 2000.

If <i>pwszAccountName</i> specifies the local system account, the caller must be an administrator on the local computer or an application running in the local system account. If not, this method will fail.

The password specified in <i>pwszPassword</i> is used to log on to the account when the work item is run. An incorrect password will result in an error when the work item is run. In the Windows Server 2003, however,  Task Scheduler validates the password at the time the job is created (during a call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a>).

Typically, passwords have an expiration date. If you schedule tasks that run indefinitely, you must update the task to reflect the new password.

 Note that errors can be returned by the initial call to 
<b>SetAccountInformation</b> or the subsequent call to <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a>.

The Task Scheduler service must be running for this call to succeed. (<b>SetAccountInformation</b> results in a remote procedure call (RPC) to the Task Scheduler service, but the RPC call is not made until <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> is called.)

The E_ACCESSDENIED return code is returned under the following conditions:

<ul>
<li>The caller does not have write access to the file that represents the scheduled work item.</li>
<li>The local account was specified (<i>pwszAccountName</i> was set to L""), but the caller is neither an administrator on the local computer nor an application running in the local system account.</li>
<li>A <b>NULL</b> password was specified in <i>pwszPassword</i>, but the caller is neither an administrator on the local computer, nor is running in the local system account.</li>
<li>The application is running under a different user name than the user named specified in the <i>pwszAccountName</i> parameter.</li>
</ul>
After setting the account information for a work item, be sure to call <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-save">IPersistFile::Save</a> to save the modified work item object to disk.


#### Examples

For more information and an example of how to set the account information of a task, see <a href="/windows/desktop/TaskSchd/c-c-code-example-setting-task-account-information">C/C++ Code Example: Setting Task Account Information</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getaccountinformation">IScheduledWorkItem::GetAccountInformation</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>