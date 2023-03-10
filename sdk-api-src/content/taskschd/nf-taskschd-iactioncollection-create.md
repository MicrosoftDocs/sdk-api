---
UID: NF:taskschd.IActionCollection.Create
title: IActionCollection::Create (taskschd.h)
description: Creates and adds a new action to the collection.
helpviewer_keywords: ["Create","Create method [Task Scheduler]","Create method [Task Scheduler]","IActionCollection interface","IActionCollection interface [Task Scheduler]","Create method","IActionCollection.Create","IActionCollection::Create","TASK_ACTION_COM_HANDLER","TASK_ACTION_EXEC","TASK_ACTION_SEND_EMAIL","TASK_ACTION_SHOW_MESSAGE","actions [Task Scheduler]","creating","taskschd.iactioncollection_create","taskschd/IActionCollection::Create"]
old-location: taskschd\iactioncollection_create.htm
tech.root: taskschd
ms.assetid: 815a000b-ba02-470d-80e6-06ba3c8ea014
ms.date: 12/05/2018
ms.keywords: Create, Create method [Task Scheduler], Create method [Task Scheduler],IActionCollection interface, IActionCollection interface [Task Scheduler],Create method, IActionCollection.Create, IActionCollection::Create, TASK_ACTION_COM_HANDLER, TASK_ACTION_EXEC, TASK_ACTION_SEND_EMAIL, TASK_ACTION_SHOW_MESSAGE, actions [Task Scheduler],creating, taskschd.iactioncollection_create, taskschd/IActionCollection::Create
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
 - IActionCollection::Create
 - taskschd/IActionCollection::Create
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
 - IActionCollection.Create
---

# IActionCollection::Create


## -description

Creates and adds a new action to the collection.

## -parameters

### -param type [in]

This parameter is set to one of the following  <a href="/windows/desktop/api/taskschd/ne-taskschd-task_action_type">TASK_ACTION_TYPE</a> enumeration constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_ACTION_EXEC"></a><a id="task_action_exec"></a><dl>
<dt><b>TASK_ACTION_EXEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The action performs a command-line operation. For example, the action could run a script, start an executable, or, if the name of a document is provided, find its associated application and start the application with the document.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_ACTION_COM_HANDLER"></a><a id="task_action_com_handler"></a><dl>
<dt><b>TASK_ACTION_COM_HANDLER</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The action fires a handler.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_ACTION_SEND_EMAIL"></a><a id="task_action_send_email"></a><dl>
<dt><b>TASK_ACTION_SEND_EMAIL</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
This action sends an email message.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_ACTION_SHOW_MESSAGE"></a><a id="task_action_show_message"></a><dl>
<dt><b>TASK_ACTION_SHOW_MESSAGE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
This action shows a message box.

</td>
</tr>
</table>

### -param ppAction [out]

An <a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a> interface that represents the new action. 

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a> interface pointer.  Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You cannot add more than 32 actions to the collection.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-iactioncollection">IActionCollection</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction">IComHandlerAction</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-iexecaction">IExecAction</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction">IShowMessageAction</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_action_type">TASK_ACTION_TYPE</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>