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

# ISyncMgrSyncCallback::CanContinue


## -description


Determines whether the synchronization has been canceled.


## -parameters




### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the ID of the item.


## -returns



Type: <b>HRESULT</b>

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>A cancellation has not been requested. The synchronization can continue.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>A cancellation has been requested. The handler should call <a href="https://msdn.microsoft.com/fd7ed6f4-49c6-44c7-86f9-0b2c04d19de8">ISyncMgrSyncCallback::ReportProgress</a>, specifying SYNCMGR_PS_CANCELED in the <i>nStatus</i> parameter.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>The value pointed to by <i>pszItemID</i> is either unknown to Sync Center or is not an item managed by this handler.</td>
</tr>
</table>
 

If <i>pszItemID</i> is <b>NULL</b> or an empty string, the return value depends on whether a cancellation has been requested for the entire handler.




## -remarks



A synchronization can be canceled by the user by clicking the <b>Stop</b> or <b>Stop All</b> task on the context menu or the command module. It can also be canceled when an application calls one of the stop methods of the <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a> interface.

By implementing this functionality as a separate method, the handler can check for a cancellation without reporting progress.


#### Examples




        	The following example shows the usage of <b>ISyncMgrSyncCallback::CanContinue</b> by the <a href="https://msdn.microsoft.com/6742f6a8-eda8-4ef0-8a11-dc70baefcc83">Synchronize</a> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CMyDeviceHandler::Synchronize(...)
{
    ...

    // Start synchronizing the sync items.

    ...

    // If a cancellation has been requested, stop the sync and exit.
    if (pCallback-&gt;CanContinue(pszItemID) == S_FALSE)
    {
        // End the sync operation and exit the function.
        hr = pCallback-&gt;ReportProgress(pszItemID,
                                       pszCancelMessage,
                                       SYNCMGR_PS_CANCELED,
                                       uCurrentStep,
                                       uMaxStep,
                                       NULL);
    }
    ...
}
</pre>
</td>
</tr>
</table></span></div>


