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

# ISyncMgrSynchronize::SetItemStatus


## -description


Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases: between the time the handler has returned from the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> method and called the 
<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a> callback method, or after the handler has returned from the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method but has not yet called the <a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a> callback method.


## -parameters




### -param pItemID [in]

Type: <b>REFGUID</b>

Identifies the item with changed status.


### -param dwSyncMgrStatus [in]

Type: <b>DWORD</b>

The new status for the specified item taken from the 
<a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a> enumeration.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values, E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, as well as the following:

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
Status was set.

</td>
</tr>
</table>
 




## -remarks



Currently, the only <a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a> status value supported by the SyncMgr is SYNCMGRSTATUS_SKIPPED. The registered application's handler should skip the item specified in <i>pItemID</i> when it receives this status value.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a>



<a href="https://msdn.microsoft.com/193926e8-824c-4969-9707-e2d95961c242">ISyncMgrSynchronize::SetProgressCallback</a>



<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a>



<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a>



<a href="https://msdn.microsoft.com/a2bdc883-2e61-42a4-a88b-8fab42f018e1">SYNCMGRSTATUS</a>



<a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a>
 

 

