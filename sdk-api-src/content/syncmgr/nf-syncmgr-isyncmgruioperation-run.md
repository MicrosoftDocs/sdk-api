---
UID: NF:syncmgr.ISyncMgrUIOperation.Run
title: ISyncMgrUIOperation::Run
author: windows-sdk-content
description: Performs the actual display of UI for a handler or sync item when requested to do so by Sync Center.
old-location: shell\ISyncMgrUIOperation_Run.htm
old-project: shell
ms.assetid: 66dd853e-0fb0-4736-982a-e0183cb51842
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ISyncMgrUIOperation interface [Windows Shell],Run method, ISyncMgrUIOperation.Run, ISyncMgrUIOperation::Run, Run, Run method [Windows Shell], Run method [Windows Shell],ISyncMgrUIOperation interface, _shell_ISyncMgrUIOperation_Run, shell.ISyncMgrUIOperation_Run, syncmgr/ISyncMgrUIOperation::Run
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrUIOperation.Run
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrUIOperation::Run


## -description


Performs the actual display of UI for a handler or sync item when requested to do so by Sync Center.


## -parameters




### -param hwndOwner [in]

Type: <b>HWND</b>

A handle to the window used to display the UI.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns S_FALSE or another error code if this method is called to confirm an operation, such as activating a handler or disabling a sync item, but that operation should not be executed.




## -remarks



The handler itself, not the UI, is expected to use the <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a> interface to notify Sync Center of changes to its state that come about through choices made by the user in the UI.


#### Examples




        	The following example shows the outline of an implementation of this method. In this case, the implementation is that which would be returned when <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">GetObject</a> is called with the SYNCMGR_OBJECTID_QueryBeforeDelete object ID.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CQueryBeforeDelete::Run(__in HWND hwndOwner)
{
    HRESULT hr = S_OK;

    // Display a dialog confirming that the user wants to delete the item.

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


