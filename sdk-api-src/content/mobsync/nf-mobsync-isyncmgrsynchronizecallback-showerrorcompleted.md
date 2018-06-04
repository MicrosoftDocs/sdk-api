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

# ISyncMgrSynchronizeCallback::ShowErrorCompleted


## -description


Called by the registered application's handler before or after its <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> operation has been completed.


## -parameters




### -param hr




### -param cItems [in]

Type: <b>ULONG</b>

The number of items in the array pointed to by the <i>pItemIDs</i> parameter. This parameter is ignored unless <i>hrResult</i> is S_SYNCMGR_RETRYSYNC.


### -param pItemIDs [in]

Type: <b>const GUID*</b>

A pointer to the array of item IDs to pass to 
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> in the event of a retry. This parameter is ignored unless <i>hrResult</i> is S_SYNCMGR_RETRYSYNC.


#### - hrResult [in]

Type: <b>HRESULT</b>

Whether <a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ShowError</a> was successful. This value is S_SYNCMGR_RETRYSYNC if the registered application's handler requires SyncMgr to retry the synchronization. When this value is returned to SyncMgr both the 
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> and <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> methods are called again.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

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
The operation completed successfully.

</td>
</tr>
</table>
 




## -remarks



The <i>pItemIDs</i> parameter is an [in] parameter and the calling function owns the memory pointed to by it. SyncMgr makes a copy of the array before returning.

The registered application's handler should return from the <a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ShowError</a> method as soon as possible and then call this method to notify SyncMgr that it has completed processing the <b>ShowError</b> call.

It is acceptable for the registered application's handler to call this method 
before returning from the <a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ShowError</a> method.

The registered application's handler should not call this method unless a success code is returned from the <a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ShowError</a> method.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ShowError</a>
 

 

