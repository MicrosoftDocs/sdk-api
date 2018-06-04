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

# ISyncMgrSynchronizeCallback::Progress


## -description


Called by a registered application to update the progress information and determine whether an operation should continue.


## -parameters




### -param ItemID [in]

Type: <b>REFGUID</b>

A reference to the item identifier for an item that is being updated.


### -param pSyncProgressItem [in]

Type: <b>const <a href="https://msdn.microsoft.com/94ac1206-be5f-467c-ab4a-11f574c406ca">SYNCMGRPROGRESSITEM</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/94ac1206-be5f-467c-ab4a-11f574c406ca">SYNCMGRPROGRESSITEM</a> structure that contains the updated progress information.


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
Continues the synchronization.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_SYNCMGR_CANCELITEM</b></dt>
</dl>
</td>
<td width="60%">
Cancels the synchronization on a specified item, as soon as possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_SYNCMGR_CANCELALL</b></dt>
</dl>
</td>
<td width="60%">
Cancels the synchronization on all items that are associated with this application, as soon as possible.

</td>
</tr>
</table>
 




## -remarks



Registered applications should call this method to provide normal feedback even when the <a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is set.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG</a>



<a href="https://msdn.microsoft.com/94ac1206-be5f-467c-ab4a-11f574c406ca">SYNCMGRPROGRESSITEM</a>
 

 

