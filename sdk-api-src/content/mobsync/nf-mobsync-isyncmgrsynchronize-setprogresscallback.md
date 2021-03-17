---
UID: NF:mobsync.ISyncMgrSynchronize.SetProgressCallback
title: ISyncMgrSynchronize::SetProgressCallback (mobsync.h)
description: Sets the ISyncMgrSynchronizeCallback interface. Registered applications use this callback interface to give status information from within the ISyncMgrSynchronize::PrepareForSync and ISyncMgrSynchronize::Synchronize methods.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","SetProgressCallback method","ISyncMgrSynchronize.SetProgressCallback","ISyncMgrSynchronize::SetProgressCallback","SetProgressCallback","SetProgressCallback method [Windows Shell]","SetProgressCallback method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::SetProgressCallback","shell.syncmgr_isyncmgrsynchronize_setprogresscallback","syncmgr.isyncmgrsynchronize_setprogresscallback"]
old-location: shell\syncmgr_isyncmgrsynchronize_setprogresscallback.htm
tech.root: shell
ms.assetid: 193926e8-824c-4969-9707-e2d95961c242
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],SetProgressCallback method, ISyncMgrSynchronize.SetProgressCallback, ISyncMgrSynchronize::SetProgressCallback, SetProgressCallback, SetProgressCallback method [Windows Shell], SetProgressCallback method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::SetProgressCallback, shell.syncmgr_isyncmgrsynchronize_setprogresscallback, syncmgr.isyncmgrsynchronize_setprogresscallback
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
 - ISyncMgrSynchronize::SetProgressCallback
 - mobsync/ISyncMgrSynchronize::SetProgressCallback
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
 - ISyncMgrSynchronize.SetProgressCallback
---

# ISyncMgrSynchronize::SetProgressCallback


## -description

Sets the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> interface. Registered applications use this callback interface to give status information from within the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> and <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> methods.

## -parameters

### -param lpCallBack [in]

Type: <b><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>*</b>

A pointer to <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> interface the registered application uses to provide feedback to SyncMgr about the synchronization status and to notify SyncMgr when the synchronization is complete.

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

Registered applications must call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">ISyncMgrSynchronizeCallback::AddRef</a> method and use it when calling SyncMgr to provide status text and progress indicator feedback.

If the registered application already has an <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> interface when the method is called, the old interface must be released and the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method of the new interface must be called. The new interface must be maintained by the registered application.

Before the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a> interface is released, SyncMgr calls this method with the <i>pSyncCallBack</i> parameter set to <b>NULL</b>. The registered application should then release the <b>ISyncMgrSynchronize</b> interface previously passed.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>