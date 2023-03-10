---
UID: NF:mobsync.ISyncMgrSynchronize.ShowError
title: ISyncMgrSynchronize::ShowError (mobsync.h)
description: Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","ShowError method","ISyncMgrSynchronize.ShowError","ISyncMgrSynchronize::ShowError","ShowError","ShowError method [Windows Shell]","ShowError method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::ShowError","shell.syncmgr_isyncmgrsynchronize_showerror","syncmgr.isyncmgrsynchronize_showerror"]
old-location: shell\syncmgr_isyncmgrsynchronize_showerror.htm
tech.root: shell
ms.assetid: 0e313c61-6482-4396-b4b8-824fba0226ac
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],ShowError method, ISyncMgrSynchronize.ShowError, ISyncMgrSynchronize::ShowError, ShowError, ShowError method [Windows Shell], ShowError method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::ShowError, shell.syncmgr_isyncmgrsynchronize_showerror, syncmgr.isyncmgrsynchronize_showerror
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
 - ISyncMgrSynchronize::ShowError
 - mobsync/ISyncMgrSynchronize::ShowError
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
 - ISyncMgrSynchronize.ShowError
---

# ISyncMgrSynchronize::ShowError


## -description

Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab.

## -parameters

### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent <b>HWND</b> that a registered application should use to display a user interface. This value can be <b>NULL</b>.

### -param ErrorID [in]

Type: <b>REFGUID</b>

An error identifier that is associated with this error message. This value is passed in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">LogError</a> method.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

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

Handlers should return as soon as possible from this method, and call the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-showerrorcompleted">ShowErrorCompleted</a> method. A handler can make a call to 
<b>ShowErrorCompleted</b> before returning from this method. If a handler returns a failure code from this method, it should not call the 
<b>ShowErrorCompleted</b> method.

Applications can display user interface elements in this method even if the 
<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is not set in the <i>dwSyncFlags</i> parameter of the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a> method. Applications must still call <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless">EnableModeless</a>, and check the return code before showing a user interface.

## -see-also

<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-enablemodeless">EnableModeless</a>



<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror">LogError</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-showerrorcompleted">ShowErrorCompleted</a>