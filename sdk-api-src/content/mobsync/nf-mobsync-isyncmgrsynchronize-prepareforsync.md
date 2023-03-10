---
UID: NF:mobsync.ISyncMgrSynchronize.PrepareForSync
title: ISyncMgrSynchronize::PrepareForSync (mobsync.h)
description: Allows a registered application to display any user interface, and perform any necessary initialization before the ISyncMgrSynchronize::Synchronize method is called.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","PrepareForSync method","ISyncMgrSynchronize.PrepareForSync","ISyncMgrSynchronize::PrepareForSync","PrepareForSync","PrepareForSync method [Windows Shell]","PrepareForSync method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::PrepareForSync","shell.syncmgr_isyncmgrsynchronize_prepareforsync","syncmgr.isyncmgrsynchronize_prepareforsync"]
old-location: shell\syncmgr_isyncmgrsynchronize_prepareforsync.htm
tech.root: shell
ms.assetid: 82e70e75-a5d4-41b2-87c4-2a032628954d
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],PrepareForSync method, ISyncMgrSynchronize.PrepareForSync, ISyncMgrSynchronize::PrepareForSync, PrepareForSync, PrepareForSync method [Windows Shell], PrepareForSync method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::PrepareForSync, shell.syncmgr_isyncmgrsynchronize_prepareforsync, syncmgr.isyncmgrsynchronize_prepareforsync
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
 - ISyncMgrSynchronize::PrepareForSync
 - mobsync/ISyncMgrSynchronize::PrepareForSync
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
 - ISyncMgrSynchronize.PrepareForSync
---

# ISyncMgrSynchronize::PrepareForSync


## -description

Allows a registered application to display any user interface, and perform any necessary initialization before the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> method is called. For example, an application such as the Microsoft Outlook email client may need to display the password dialog box to enable a user to log on to a mail server.

## -parameters

### -param cbNumItems [in]

Type: <b>ULONG</b>

The number of items in the array pointed to by <i>pItemIDs</i>.

### -param pItemIDs [in]

Type: <b>GUID*</b>

An array of item IDs that a user chooses to synchronize.

### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent <b>HWND</b> that a registered application should use for any user interface element displayed. This value may be <b>NULL</b>.

### -param dwReserved [in]

Type: <b>DWORD</b>

Reserved. Registered applications should ignore this value.

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
Preparation is successful.

</td>
</tr>
</table>

## -remarks

A registered application handler should return from this method as soon as possible, and then call the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted">PrepareForSyncCompleted</a> method. A registered application handler can call the <b>PrepareForSyncCompleted</b> method before returning from this method.

Registered applications should only show a user interface if the 
<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is set in the <i>dwSyncFlags</i> parameter of the 
<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a> method. If a registered application cannot prepare for synchronization without showing a user interface when the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG_MAYBOTHERUSER</a> flag is not set, it should return S_FALSE from this method.

The array of item IDs that are passed into this method are relevant to the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a> method also.

The <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a> methods can be called on any thread in a registered application.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">ISyncMgrSynchronize::Initialize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-synchronize">ISyncMgrSynchronize::Synchronize</a>



<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizecallback-prepareforsynccompleted">PrepareForSyncCompleted</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a>