---
UID: NF:syncmgr.ISyncMgrSyncResult.Result
title: ISyncMgrSyncResult::Result (syncmgr.h)
description: Gets the result of a StartHandlerSync or StartItemSync call.
helpviewer_keywords: ["ISyncMgrSyncResult interface [Windows Shell]","Result method","ISyncMgrSyncResult.Result","ISyncMgrSyncResult::Result","Result","Result method [Windows Shell]","Result method [Windows Shell]","ISyncMgrSyncResult interface","_shell_ISyncMgrSyncResult_Result","shell.ISyncMgrSyncResult_Result","syncmgr/ISyncMgrSyncResult::Result"]
old-location: shell\ISyncMgrSyncResult_Result.htm
tech.root: shell
ms.assetid: 8ba7de05-0703-4bab-bf64-ae84f42fad69
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncResult interface [Windows Shell],Result method, ISyncMgrSyncResult.Result, ISyncMgrSyncResult::Result, Result, Result method [Windows Shell], Result method [Windows Shell],ISyncMgrSyncResult interface, _shell_ISyncMgrSyncResult_Result, shell.ISyncMgrSyncResult_Result, syncmgr/ISyncMgrSyncResult::Result
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSyncResult::Result
 - syncmgr/ISyncMgrSyncResult::Result
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncResult.Result
---

# ISyncMgrSyncResult::Result


## -description

Gets the result of a <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync">StartHandlerSync</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync">StartItemSync</a> call.

## -parameters

### -param nStatus [in]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PROGRESS_STATUS</a></b>

The current status of the progress report. See <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_progress_status">SYNCMGR_PROGRESS_STATUS</a>.

### -param cError [in]

Type: <b>UINT</b>

An error.

### -param cConflicts [in]

Type: <b>UINT</b>

Specifies conflicts.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.