---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.DeleteLogError
title: ISyncMgrSynchronizeCallback::DeleteLogError (mobsync.h)
description: Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box.
helpviewer_keywords: ["DeleteLogError","DeleteLogError method [Windows Shell]","DeleteLogError method [Windows Shell]","ISyncMgrSynchronizeCallback interface","ISyncMgrSynchronizeCallback interface [Windows Shell]","DeleteLogError method","ISyncMgrSynchronizeCallback.DeleteLogError","ISyncMgrSynchronizeCallback::DeleteLogError","mobsync/ISyncMgrSynchronizeCallback::DeleteLogError","shell.syncmgr_isyncmgrsynchronizecallback_deletelogerror","syncmgr.isyncmgrsynchronizecallback_deletelogerror"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_deletelogerror.htm
tech.root: shell
ms.assetid: 06e90b81-14cc-4b3e-9d2d-30e60eeb8eb2
ms.date: 12/05/2018
ms.keywords: DeleteLogError, DeleteLogError method [Windows Shell], DeleteLogError method [Windows Shell],ISyncMgrSynchronizeCallback interface, ISyncMgrSynchronizeCallback interface [Windows Shell],DeleteLogError method, ISyncMgrSynchronizeCallback.DeleteLogError, ISyncMgrSynchronizeCallback::DeleteLogError, mobsync/ISyncMgrSynchronizeCallback::DeleteLogError, shell.syncmgr_isyncmgrsynchronizecallback_deletelogerror, syncmgr.isyncmgrsynchronizecallback_deletelogerror
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
 - ISyncMgrSynchronizeCallback::DeleteLogError
 - mobsync/ISyncMgrSynchronizeCallback::DeleteLogError
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
 - ISyncMgrSynchronizeCallback.DeleteLogError
---

# ISyncMgrSynchronizeCallback::DeleteLogError


## -description

Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box.

## -parameters

### -param ErrorID [in]

Type: <b>REFGUID</b>

The LogError to be deleted. If <i>ErrorID</i> is GUID_NULL all errors logged by the instance of the registered application's handler will be deleted.

### -param dwReserved [in]

Type: <b>DWORD</b>

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, as well as the following:

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
The item was successfully deleted from the log.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>