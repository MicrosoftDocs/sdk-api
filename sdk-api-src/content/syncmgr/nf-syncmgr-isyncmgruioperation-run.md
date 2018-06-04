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


