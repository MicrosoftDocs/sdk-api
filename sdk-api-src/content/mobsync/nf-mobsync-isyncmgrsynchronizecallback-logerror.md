---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.LogError
title: ISyncMgrSynchronizeCallback::LogError (mobsync.h)
description: Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.
helpviewer_keywords: ["ISyncMgrSynchronizeCallback interface [Windows Shell]","LogError method","ISyncMgrSynchronizeCallback.LogError","ISyncMgrSynchronizeCallback::LogError","LogError","LogError method [Windows Shell]","LogError method [Windows Shell]","ISyncMgrSynchronizeCallback interface","mobsync/ISyncMgrSynchronizeCallback::LogError","shell.syncmgr_isyncmgrsynchronizecallback_logerror","syncmgr.isyncmgrsynchronizecallback_logerror"]
old-location: shell\syncmgr_isyncmgrsynchronizecallback_logerror.htm
tech.root: shell
ms.assetid: 7c25ef21-9815-41ad-bcc0-b41a62dc0fe5
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],LogError method, ISyncMgrSynchronizeCallback.LogError, ISyncMgrSynchronizeCallback::LogError, LogError, LogError method [Windows Shell], LogError method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::LogError, shell.syncmgr_isyncmgrsynchronizecallback_logerror, syncmgr.isyncmgrsynchronizecallback_logerror
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
 - ISyncMgrSynchronizeCallback::LogError
 - mobsync/ISyncMgrSynchronizeCallback::LogError
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
 - ISyncMgrSynchronizeCallback.LogError
---

# ISyncMgrSynchronizeCallback::LogError


## -description

Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.

## -parameters

### -param dwErrorLevel [in]

Type: <b>DWORD</b>

The error level. Values are taken from the <a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrloglevel">SYNCMGRLOGLEVEL</a> enumeration.

### -param pszErrorText [in]

Type: <b>LPCWSTR</b>

A pointer to error text to be displayed in the error tab.

### -param pSyncLogError [in]

Type: <b>const <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrlogerrorinfo">SYNCMGRLOGERRORINFO</a>*</b>

A pointer to the <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrlogerrorinfo">SYNCMGRLOGERRORINFO</a> structure that contains additional error information. Registered applications that do not provide this data can pass <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and  the following:

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
The error information is logged successfully.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>



<a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrlogerrorinfo">SYNCMGRLOGERRORINFO</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgrloglevel">SYNCMGRLOGLEVEL</a>