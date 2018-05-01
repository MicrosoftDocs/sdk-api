---
UID: NF:mobsync.ISyncMgrSynchronize.SetProgressCallback
title: ISyncMgrSynchronize::SetProgressCallback method
author: windows-driver-content
description: Sets the ISyncMgrSynchronizeCallback interface. Registered applications use this callback interface to give status information from within the ISyncMgrSynchronize::PrepareForSync and ISyncMgrSynchronize::Synchronize methods.
old-location: shell\syncmgr_isyncmgrsynchronize_setprogresscallback.htm
old-project: shell
ms.assetid: 193926e8-824c-4969-9707-e2d95961c242
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ISyncMgrSynchronize, ISyncMgrSynchronize interface [Windows Shell], SetProgressCallback method, ISyncMgrSynchronize::SetProgressCallback, SetProgressCallback method [Windows Shell], SetProgressCallback method [Windows Shell], ISyncMgrSynchronize interface, SetProgressCallback,ISyncMgrSynchronize.SetProgressCallback, mobsync/ISyncMgrSynchronize::SetProgressCallback, shell.syncmgr_isyncmgrsynchronize_setprogresscallback, syncmgr.isyncmgrsynchronize_setprogresscallback
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
req.typenames: SYNCMGRSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mobsync.dll
api_name:
-	ISyncMgrSynchronize.SetProgressCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronize::SetProgressCallback method


## -description


Sets the <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> interface. Registered applications use this callback interface to give status information from within the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> and <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> methods.


## -parameters




### -param lpCallBack






#### - pSyncCallBack [in]

Type: <b><a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>*</b>

A pointer to <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> interface the registered application uses to provide feedback to SyncMgr about the synchronization status and to notify SyncMgr when the synchronization is complete.


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
Synchronization callback interface was successfully set.

</td>
</tr>
</table>
 




## -remarks



Registered applications must call the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">ISyncMgrSynchronizeCallback::AddRef</a> method and use it when calling SyncMgr to provide status text and progress indicator feedback.

If the registered application already has an <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> interface when the method is called, the old interface must be released and the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method of the new interface must be called. The new interface must be maintained by the registered application.

Before the <a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a> interface is released, SyncMgr calls this method with the <i>pSyncCallBack</i> parameter set to <b>NULL</b>. The registered application should then release the <b>ISyncMgrSynchronize</b> interface previously passed.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>
 

 

