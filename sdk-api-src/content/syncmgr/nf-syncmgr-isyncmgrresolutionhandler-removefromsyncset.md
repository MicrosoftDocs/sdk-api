---
UID: NF:syncmgr.ISyncMgrResolutionHandler.RemoveFromSyncSet
title: ISyncMgrResolutionHandler::RemoveFromSyncSet (syncmgr.h)
description: Deletes the conflict and removes the IShellItem from synchronization.
helpviewer_keywords: ["ISyncMgrResolutionHandler interface [Windows Shell]","RemoveFromSyncSet method","ISyncMgrResolutionHandler.RemoveFromSyncSet","ISyncMgrResolutionHandler::RemoveFromSyncSet","RemoveFromSyncSet","RemoveFromSyncSet method [Windows Shell]","RemoveFromSyncSet method [Windows Shell]","ISyncMgrResolutionHandler interface","_shell_ISyncMgrResolutionHandler_RemoveFromSyncSet","shell.ISyncMgrResolutionHandler_RemoveFromSyncSet","syncmgr/ISyncMgrResolutionHandler::RemoveFromSyncSet"]
old-location: shell\ISyncMgrResolutionHandler_RemoveFromSyncSet.htm
tech.root: shell
ms.assetid: 3f65f844-efa2-43b9-91f2-c9c0ed4e3a9e
ms.date: 12/05/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],RemoveFromSyncSet method, ISyncMgrResolutionHandler.RemoveFromSyncSet, ISyncMgrResolutionHandler::RemoveFromSyncSet, RemoveFromSyncSet, RemoveFromSyncSet method [Windows Shell], RemoveFromSyncSet method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_RemoveFromSyncSet, shell.ISyncMgrResolutionHandler_RemoveFromSyncSet, syncmgr/ISyncMgrResolutionHandler::RemoveFromSyncSet
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
 - ISyncMgrResolutionHandler::RemoveFromSyncSet
 - syncmgr/ISyncMgrResolutionHandler::RemoveFromSyncSet
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
 - ISyncMgrResolutionHandler.RemoveFromSyncSet
---

# ISyncMgrResolutionHandler::RemoveFromSyncSet


## -description

Deletes the conflict and removes the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>  from synchronization.

## -parameters

### -param pFeedback [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

A pointer to a <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> that is in conflict will no longer be synchronized and the conflict should be deleted.

The <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value returned in <i>pFeedback</i> determines how the next conflict is resolved. If this method fails, an error message is displayed and the user is asked how to proceed.