---
UID: NF:taskschd.ITaskService.Connect
title: ITaskService::Connect (taskschd.h)
description: Connects to a remote computer and associates all subsequent calls on this interface with a remote session.
helpviewer_keywords: ["Connect","Connect method [Task Scheduler]","Connect method [Task Scheduler]","ITaskService interface","ITaskService interface [Task Scheduler]","Connect method","ITaskService.Connect","ITaskService::Connect","taskschd.itaskservice_connect","taskschd/ITaskService::Connect"]
old-location: taskschd\itaskservice_connect.htm
tech.root: taskschd
ms.assetid: ba810bac-e587-4eb8-871c-449b4174ab46
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [Task Scheduler], Connect method [Task Scheduler],ITaskService interface, ITaskService interface [Task Scheduler],Connect method, ITaskService.Connect, ITaskService::Connect, taskschd.itaskservice_connect, taskschd/ITaskService::Connect
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskService::Connect
 - taskschd/ITaskService::Connect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskService.Connect
---

# ITaskService::Connect


## -description

Connects to a remote computer and associates all subsequent calls on this interface with a remote session. If the <i>serverName</i> parameter is empty, then this method will execute on the local computer. If the <i>user</i> is not specified, then the current token is used.

## -parameters

### -param serverName [in, optional]

The name of the computer that you want to connect to. If the <i>serverName</i> parameter is empty, then this method will execute on the local computer.

### -param user [in, optional]

The user name that is used during the connection to the computer. If the <i>user</i> is not specified, then the current token is used.

### -param domain [in, optional]

The domain of the user specified in the <i>user</i> parameter.

### -param password [in, optional]

The password that is used to connect to the computer. If the user name and password are not specified, then the current token is used.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
<dt>0x80070005</dt>
</dl>
</td>
<td width="60%">
Access is denied to connect to the Task Scheduler service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_SERVICE_NOT_RUNNING</b></dt>
<dt>0x80041315</dt>
</dl>
</td>
<td width="60%">
The Task Scheduler service is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000e</dt>
</dl>
</td>
<td width="60%">
The application does not have enough memory to complete the operation or the <i>user</i>, <i>password</i>, or <i>domain</i> has at least one null and one non-null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_NETPATH</b></dt>
<dt>53</dt>
</dl>
</td>
<td width="60%">
This error is returned in the following situations:

<ul>
<li>The computer name specified in the <i>serverName</i> parameter does not exist.</li>
<li>When you are trying to connect to a Windows Server 2003 or Windows XP computer, and the remote computer does not have the File and Printer Sharing firewall exception enabled or the Remote Registry service is not running.</li>
<li>When you are trying to connect to a Windows Vista computer, and the remote computer does not have the Remote Scheduled Tasks Management firewall exception enabled and the File and Printer Sharing firewall exception enabled, or the Remote Registry service is not running.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt>50</dt>
</dl>
</td>
<td width="60%">
The <i>user</i>, <i>password</i>, or <i>domain</i> parameters cannot be specified when connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer.



</td>
</tr>
</table>

## -remarks

The <b>ITaskService::Connect</b> method should be called before calling any of the other <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskservice">ITaskService</a> methods.

If you are to connecting to a remote Windows Vista computer from a Windows Vista, you need to allow the Remote Scheduled Tasks Management firewall exception on the remote computer. To allow this exception click <b>Start</b>, <b>Control Panel</b>, <b>Security</b>, <b>Allow a program through Windows Firewall</b>, and then select the <b>Remote Scheduled Tasks Management</b> check box. Then click the <b>Ok</b> button in the Windows Firewall Settings dialog box.

If you are connecting to a remote Windows XP or Windows Server 2003 computer from a Windows Vista computer, you need to allow the File and Printer Sharing firewall exception on the remote computer. To allow this exception click <b>Start</b>, <b>Control Panel</b>, double-click <b>Windows Firewall</b>, select the <b>Exceptions</b> tab, and then select the <b>File and Printer Sharing</b> firewall exception. Then click the <b>OK</b> button in the Windows Firewall dialog box. The Remote Registry service must also be running on the remote computer.


<div class="alert"><b>Note</b>  The <b>ITaskService::Connect</b> may return an  error <b>SCHED_E_INVALIDVALUE</b> while reading the task definition if the schema of the remote task is not supported by the current machine. To verify the highest schema version supported by the current machine, check the <a href="/windows/desktop/TaskSchd/taskservice-highestversion"> ITaskService::HighestVersion</a> property.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskservice">ITaskService</a>



<a href="/windows/desktop/TaskSchd/taskservice-highestversion"> ITaskService::HighestVersion</a>