---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.PrepareForSyncCompleted
title: ISyncMgrSynchronizeCallback::PrepareForSyncCompleted
author: windows-sdk-content
description: Called by a registered handler of an application after the PrepareForSync method is complete.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_prepareforsynccompleted.htm
tech.root: shell
ms.assetid: 2ba73e09-c01b-44af-8979-8aae450c9c0b
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],PrepareForSyncCompleted method, ISyncMgrSynchronizeCallback.PrepareForSyncCompleted, ISyncMgrSynchronizeCallback::PrepareForSyncCompleted, PrepareForSyncCompleted, PrepareForSyncCompleted method [Windows Shell], PrepareForSyncCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::PrepareForSyncCompleted, shell.syncmgr_isyncmgrsynchronizecallback_prepareforsynccompleted, syncmgr.isyncmgrsynchronizecallback_prepareforsynccompleted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mobsync.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeCallback.PrepareForSyncCompleted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeCallback::PrepareForSyncCompleted


## -description


Called by a registered handler of an application after the 
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> method is complete.


## -parameters




### -param hr [in]

Type: <b>HRESULT</b>

The return value of the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> method. If S_OK is returned, the synchronization manager calls <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> for the item. If the <b>HRESULT</b> is set to anything other than S_OK, the synchronization manager releases the handler without calling the <b>Synchronize</b> method.


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
The call is completed successfully.

</td>
</tr>
</table>
 




## -remarks



A registered handler of an application should return as soon as possible from the 
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> method, and then call this method to notify the synchronization manager  that the registered application is preparing for synchronization.

It is acceptable for the registered handler of an application to call this method before returning from the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> method.

The registered handler of an application should not call this method if the 
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a> method returns any value that is different from S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a>



<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a>
 

 

