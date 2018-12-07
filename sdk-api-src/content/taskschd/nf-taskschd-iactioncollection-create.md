---
UID: NF:taskschd.IActionCollection.Create
title: IActionCollection::Create
author: windows-sdk-content
description: Creates and adds a new action to the collection.
old-location: taskschd\iactioncollection_create.htm
tech.root: taskschd
ms.assetid: 815a000b-ba02-470d-80e6-06ba3c8ea014
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Create, Create method [Task Scheduler], Create method [Task Scheduler],IActionCollection interface, IActionCollection interface [Task Scheduler],Create method, IActionCollection.Create, IActionCollection::Create, TASK_ACTION_COM_HANDLER, TASK_ACTION_EXEC, TASK_ACTION_SEND_EMAIL, TASK_ACTION_SHOW_MESSAGE, actions [Task Scheduler],creating, taskschd.iactioncollection_create, taskschd/IActionCollection::Create
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IActionCollection.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActionCollection::Create


## -description


Creates and adds a new action to the collection.


## -parameters




### -param type [in]

This parameter is set to one of the following  <a href="https://msdn.microsoft.com/931ea805-fc73-4717-ab40-c12767930df3">TASK_ACTION_TYPE</a> enumeration constants.

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

An <a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a> interface that represents the new action. 

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a> interface pointer.  Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



You cannot add more than 32 actions to the collection.




## -see-also




<a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a>



<a href="https://msdn.microsoft.com/aa7781b6-2600-4af5-95b8-2ac7928946fa">IActionCollection</a>



<a href="https://msdn.microsoft.com/fb5cc2c3-ba86-401a-b51f-b28d1f5be58f">IComHandlerAction</a>



<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>



<a href="https://msdn.microsoft.com/46a4cd60-df23-4109-8a86-b7755a6922dd">IExecAction</a>



<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>



<a href="https://msdn.microsoft.com/931ea805-fc73-4717-ab40-c12767930df3">TASK_ACTION_TYPE</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

