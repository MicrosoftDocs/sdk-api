---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.SynchronizeCompleted
title: ISyncMgrSynchronizeCallback::SynchronizeCompleted
author: windows-sdk-content
description: Called by an application when its Synchronize method is complete.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_synchronizecompleted.htm
old-project: shell
ms.assetid: df0f0e20-6b84-4ff1-badb-40006a4b8e2c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],SynchronizeCompleted method, ISyncMgrSynchronizeCallback.SynchronizeCompleted, ISyncMgrSynchronizeCallback::SynchronizeCompleted, SynchronizeCompleted, SynchronizeCompleted method [Windows Shell], SynchronizeCompleted method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::SynchronizeCompleted, shell.syncmgr_isyncmgrsynchronizecallback_synchronizecompleted, syncmgr.isyncmgrsynchronizecallback_synchronizecompleted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SYNCMGRSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeCallback.SynchronizeCompleted
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronizeCallback::SynchronizeCompleted


## -description


Called by an application when its <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> method is complete.


## -parameters




### -param hr [in]

Type: <b>HRESULT</b>

The returned result from the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> method.


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



A registered handler of an application should return from the 
<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> method as soon as possible, and then call this method to notify the synchronization manager that the synchronization process is complete.

It is acceptable for a registered handler of an application to call this method before returning from the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> method.

However, the registered handler of an application should not call this method if the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a> method returns any value that is different from S_OK.




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a>
 

 

