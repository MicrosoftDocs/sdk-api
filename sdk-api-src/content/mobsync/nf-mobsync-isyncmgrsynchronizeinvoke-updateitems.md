---
UID: NF:mobsync.ISyncMgrSynchronizeInvoke.UpdateItems
title: ISyncMgrSynchronizeInvoke::UpdateItems (mobsync.h)
description: Programmatically starts an update for specified items.
helpviewer_keywords: ["ISyncMgrSynchronizeInvoke interface [Windows Shell]","UpdateItems method","ISyncMgrSynchronizeInvoke.UpdateItems","ISyncMgrSynchronizeInvoke::UpdateItems","UpdateItems","UpdateItems method [Windows Shell]","UpdateItems method [Windows Shell]","ISyncMgrSynchronizeInvoke interface","mobsync/ISyncMgrSynchronizeInvoke::UpdateItems","shell.syncmgr_isyncmgrsynchronizeinvoke_updateitems","syncmgr.isyncmgrsynchronizeinvoke_updateitems"]
old-location: shell\syncmgr_isyncmgrsynchronizeinvoke_updateitems.htm
tech.root: shell
ms.assetid: 7a646d11-a84c-44c1-b52b-ffd364cc2ac3
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeInvoke interface [Windows Shell],UpdateItems method, ISyncMgrSynchronizeInvoke.UpdateItems, ISyncMgrSynchronizeInvoke::UpdateItems, UpdateItems, UpdateItems method [Windows Shell], UpdateItems method [Windows Shell],ISyncMgrSynchronizeInvoke interface, mobsync/ISyncMgrSynchronizeInvoke::UpdateItems, shell.syncmgr_isyncmgrsynchronizeinvoke_updateitems, syncmgr.isyncmgrsynchronizeinvoke_updateitems
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
 - ISyncMgrSynchronizeInvoke::UpdateItems
 - mobsync/ISyncMgrSynchronizeInvoke::UpdateItems
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
 - ISyncMgrSynchronizeInvoke.UpdateItems
---

# ISyncMgrSynchronizeInvoke::UpdateItems


## -description

Programmatically starts an update for specified items.

## -parameters

### -param dwInvokeFlags [in]

Type: <b>DWORD</b>

Specifies how an item should be invoked using the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrinvokeflags">SYNCMGRINVOKEFLAGS</a> enumeration values.

### -param clsid [in]

Type: <b>REFCLSID</b>

The CLSID of a registered application to be invoked for an update.

### -param cbCookie [in]

Type: <b>DWORD</b>

The size of <i>pCookie</i> data, in bytes.

### -param pCookie [in]

Type: <b>const BYTE*</b>

A pointer to a private token that identifies an application. The token is passed in the <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">Initialize</a> method.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED and E_OUTOFMEMORY, and the following:

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
The synchronization is successfully updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The errors occur during a synchronization update.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizeinvoke">ISyncMgrSynchronizeInvoke</a>



<a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-initialize">Initialize</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrinvokeflags">SYNCMGRINVOKEFLAGS</a>