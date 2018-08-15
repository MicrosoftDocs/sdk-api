---
UID: NF:mobsync.ISyncMgrSynchronize.Synchronize
title: ISyncMgrSynchronize::Synchronize
author: windows-sdk-content
description: Called by the synchronization manager once for each selected group after the user has chosen the registered applications to be synchronized.
old-location: shell\syncmgr_isyncmgrsynchronize_synchronize.htm
old-project: shell
ms.assetid: 78c202dd-9f8c-43c1-a7be-48030bc34a9c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],Synchronize method, ISyncMgrSynchronize.Synchronize, ISyncMgrSynchronize::Synchronize, Synchronize, Synchronize method [Windows Shell], Synchronize method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::Synchronize, shell.syncmgr_isyncmgrsynchronize_synchronize, syncmgr.isyncmgrsynchronize_synchronize
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
 - ISyncMgrSynchronize.Synchronize
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronize::Synchronize


## -description


Called by the synchronization manager once for each selected group after the user has chosen the registered applications to be synchronized.


## -parameters




### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent <b>HWND</b> the registered application should use for any user interface elements that it displays. This value may be <b>NULL</b>.


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
Synchronization was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Synchronization failed.

</td>
</tr>
</table>
 




## -remarks



If the user does not select any item choices for the registered application, the <b>ISyncMgrSynchronize::Synchronize</b> method is not called and the interface is released. If this method is called, the application must synchronize the items that were specified in the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> method.

The registered application's handler should return from the <b>ISyncMgrSynchronize::Synchronize</b> method as soon as possible and then call the 
<a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a> method. It is acceptable for the handler to call the <b>SynchronizeCompleted</b> call before returning from the <b>ISyncMgrSynchronize::Synchronize</b> method.

The application must give progress feedback and check whether the synchronization should be canceled by using the <i>pSyncCallBack</i> interface pointer that was set up in the <a href="https://msdn.microsoft.com/193926e8-824c-4969-9707-e2d95961c242">ISyncMgrSynchronize::SetProgressCallback</a> method.

Applications must provide progress information even if the 
<a href="https://msdn.microsoft.com/b1a60a6b-b4f8-4c89-853b-5a5584c415e9">SYNCMGRFLAG_MAYBOTHERUSER</a> flag was not specified in <a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a>.

Applications should try not to show user interface elements from within the 
<b>ISyncMgrSynchronize::Synchronize</b> method. Any user interface elements should be shown in the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> and <a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ISyncMgrSynchronize::ShowError</a> methods so the end user experiences a consistent user interface which is limited to logon and to specifying shares to be synchronized. Subsequently, the synchronization can be performed without any user intervention. After the synchronization is complete, conflicts or other error messages can be shown.

The <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> methods can be called on any thread in your application.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>



<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">ISyncMgrSynchronize::Initialize</a>



<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a>



<a href="https://msdn.microsoft.com/193926e8-824c-4969-9707-e2d95961c242">ISyncMgrSynchronize::SetProgressCallback</a>



<a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ISyncMgrSynchronize::ShowError</a>



<a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a>
 

 

