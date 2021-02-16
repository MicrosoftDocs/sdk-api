---
UID: NF:mobsync.ISyncMgrSynchronize.Synchronize
title: ISyncMgrSynchronize::Synchronize (mobsync.h)
description: Called by the synchronization manager once for each selected group after the user has chosen the registered applications to be synchronized.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","Synchronize method","ISyncMgrSynchronize.Synchronize","ISyncMgrSynchronize::Synchronize","Synchronize","Synchronize method [Windows Shell]","Synchronize method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::Synchronize","shell.syncmgr_isyncmgrsynchronize_synchronize","syncmgr.isyncmgrsynchronize_synchronize"]
old-location: shell\syncmgr_isyncmgrsynchronize_synchronize.htm
tech.root: shell
ms.assetid: 78c202dd-9f8c-43c1-a7be-48030bc34a9c
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],Synchronize method, ISyncMgrSynchronize.Synchronize, ISyncMgrSynchronize::Synchronize, Synchronize, Synchronize method [Windows Shell], Synchronize method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::Synchronize, shell.syncmgr_isyncmgrsynchronize_synchronize, syncmgr.isyncmgrsynchronize_synchronize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSynchronize::Synchronize
 - mobsync/ISyncMgrSynchronize::Synchronize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize.Synchronize
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

If the user does not select any item choices for the registered application, the <b>ISyncMgrSynchronize::Synchronize</b> method is not called and the interface is released. If this method is called, the application must synchronize the items that were specified in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> method.

The registered application's handler should return from the <b>ISyncMgrSynchronize::Synchronize</b> method as soon as possible and then call the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">SynchronizeCompleted</a> method. It is acceptable for the handler to call the <b>SynchronizeCompleted</b> call before returning from the <b>ISyncMgrSynchronize::Synchronize</b> method.

The application must give progress feedback and check whether the synchronization should be canceled by using the <i>pSyncCallBack</i> interface pointer that was set up in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback">ISyncMgrSynchronize::SetProgressCallback</a> method.

Applications must provide progress information even if the 
<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG_MAYBOTHERUSER</a> flag was not specified in <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a>.

Applications should try not to show user interface elements from within the 
<b>ISyncMgrSynchronize::Synchronize</b> method. Any user interface elements should be shown in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> and <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ISyncMgrSynchronize::ShowError</a> methods so the end user experiences a consistent user interface which is limited to logon and to specifying shares to be synchronized. Subsequently, the synchronization can be performed without any user intervention. After the synchronization is complete, conflicts or other error messages can be shown.

The <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> methods can be called on any thread in your application.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-setprogresscallback">ISyncMgrSynchronize::SetProgressCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-showerror">ISyncMgrSynchronize::ShowError</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-synchronizecompleted">SynchronizeCompleted</a>