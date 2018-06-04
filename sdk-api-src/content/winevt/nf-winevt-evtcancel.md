---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# EvtCancel function


## -description


Cancels all pending operations on a handle.


## -parameters




### -param Object

The handle whose operation you want to cancel. You can cancel the following operations:

<ul>
<li>
<a href="https://msdn.microsoft.com/26d2aabd-96dc-4091-82f4-e5d4c69e09a4">EvtClearLog</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c177029f-84e3-41ec-bbdb-26b0c1bf481f">EvtExportLog</a>
</li>
<li>
<a href="https://msdn.microsoft.com/46d40734-f022-4775-aa4f-13f4069c43c8">EvtNext</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>
</li>
<li>
<a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a>
</li>
<li>
<a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a>
</li>
</ul>
To cancel the <a href="https://msdn.microsoft.com/26d2aabd-96dc-4091-82f4-e5d4c69e09a4">EvtClearLog</a>, 
       <a href="https://msdn.microsoft.com/c177029f-84e3-41ec-bbdb-26b0c1bf481f">EvtExportLog</a>, 
       <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>, and 
       <a href="https://msdn.microsoft.com/e7c4c5f9-2a5a-4004-8f19-13eb61c4346b">EvtSubscribe</a> operations, you must pass the session 
       handle. To specify the default session (local session), set this parameter to 
       <b>NULL</b>.


## -returns



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The function failed. To get the error code, call the 
        <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

</td>
</tr>
</table>
 




## -remarks



Use this function to cancel long-running operations. For example, calling the 
    <a href="https://msdn.microsoft.com/46d40734-f022-4775-aa4f-13f4069c43c8">EvtNext</a> function could theoretically take a long time due to 
    the filtering of thousands of event records.  Calling 
    <b>EvtCancel</b> would stop the 
    <b>EvtNext</b> function from processing further event records. Note 
    that the function may not be able to stop the operation immediately.

You must call the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function to close the handle 
    when done.

The following procedure describes how to cancel a long-running operation.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b>To cancel a long-running operation</b>

<ol>
<li>Thread A calls a long running operation (for example,  the 
      <a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a> function).</li>
<li>Thread B wants to cancel and close all operations, so thread B calls the 
      <b>EvtCancel</b> function.</li>
<li>Thread B then waits for all pending calls to complete (by synchronizing with thread A). Because the 
      <b>EvtCancel</b> function was called, thread A should complete 
      soon after the call to the <b>EvtCancel</b> was made.</li>
<li>After thread A has fully completed the operation 
      (<a href="https://msdn.microsoft.com/62cf5039-f7c5-4f16-b7e3-dcc8907e6b7c">EvtSeek</a>), thread B can close the query result handle using 
      the <a href="https://msdn.microsoft.com/c4b82d7b-508d-45bf-b990-04e90e846525">EvtClose</a> function.</li>
</ol>
The operation being stopped will return with an error code of ERROR_CANCELLED.



