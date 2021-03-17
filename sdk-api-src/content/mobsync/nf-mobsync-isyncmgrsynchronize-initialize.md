---
UID: NF:mobsync.ISyncMgrSynchronize.Initialize
title: ISyncMgrSynchronize::Initialize (mobsync.h)
description: Called by the synchronization manager in a registered application handler to determine whether the handler processes the synchronization event.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","Initialize method","ISyncMgrSynchronize.Initialize","ISyncMgrSynchronize::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::Initialize","shell.syncmgr_isyncmgrsynchronize_initialize","syncmgr.isyncmgrsynchronize_initialize"]
old-location: shell\syncmgr_isyncmgrsynchronize_initialize.htm
tech.root: shell
ms.assetid: 4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],Initialize method, ISyncMgrSynchronize.Initialize, ISyncMgrSynchronize::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::Initialize, shell.syncmgr_isyncmgrsynchronize_initialize, syncmgr.isyncmgrsynchronize_initialize
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
 - ISyncMgrSynchronize::Initialize
 - mobsync/ISyncMgrSynchronize::Initialize
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
 - ISyncMgrSynchronize.Initialize
---

# ISyncMgrSynchronize::Initialize


## -description

Called by the synchronization manager in a registered application handler to determine whether the handler processes the synchronization event.

## -parameters

### -param dwReserved [in]

Type: <b>DWORD</b>

Reserved; must be 0 (zero).

### -param dwSyncMgrFlags [in]

Type: <b>DWORD</b>

The <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a> enumeration values that describe how a synchronization event is initiated.

### -param cbCookie [in]

Type: <b>DWORD</b>

The size of the <i>lpCookie</i> data, in bytes.

### -param lpCookie [in]

Type: <b>BYTE const*</b>

A pointer to the token that identifies an application. This token is passed when an application invokes the synchronization manager programmatically.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following.

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
Initialization is successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Application handler does not process a synchronization event.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a> enumeration values apply through the lifetime of the <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a> interface, and are used by the other 
<b>ISyncMgrSynchronize</b> methods.

If an application does not recognize the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a> event, the application should treat the event as a manual synchronization.

A registered application handler cannot display a user interface within this call unless it is the first time the initialization method is called. An application can display any one-time initialization it needs to set up items and introduce a user to an application feature. If you need to display a user interface for a different reason as part of the synchronization process, you can use the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a> method.

The <i>lpCookie</i> parameter is <b>NULL</b> unless a handling application invokes the synchronization manager programmatically by using <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems">UpdateItems</a>. In this scenario, the class identifier (CLSID) identifies the handling application, and the value of <i>lpCookie</i> is passed in by the handling application, and then passed back by the synchronization manager during synchronization for context. The <i>lpCookie</i> parameter is only meaningful when <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG_INVOKE</a> is set.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-prepareforsync">ISyncMgrSynchronize::PrepareForSync</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrflag">SYNCMGRFLAG</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems">UpdateItems</a>