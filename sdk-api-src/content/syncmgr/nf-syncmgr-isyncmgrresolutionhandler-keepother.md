---
UID: NF:syncmgr.ISyncMgrResolutionHandler.KeepOther
title: ISyncMgrResolutionHandler::KeepOther (syncmgr.h)
description: Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals.
helpviewer_keywords: ["ISyncMgrResolutionHandler interface [Windows Shell]","KeepOther method","ISyncMgrResolutionHandler.KeepOther","ISyncMgrResolutionHandler::KeepOther","KeepOther","KeepOther method [Windows Shell]","KeepOther method [Windows Shell]","ISyncMgrResolutionHandler interface","_shell_ISyncMgrResolutionHandler_KeepOther","shell.ISyncMgrResolutionHandler_KeepOther","syncmgr/ISyncMgrResolutionHandler::KeepOther"]
old-location: shell\ISyncMgrResolutionHandler_KeepOther.htm
tech.root: shell
ms.assetid: 6d3e3b01-447c-4f7b-8a63-5bd9084de00a
ms.date: 12/05/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],KeepOther method, ISyncMgrResolutionHandler.KeepOther, ISyncMgrResolutionHandler::KeepOther, KeepOther, KeepOther method [Windows Shell], KeepOther method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_KeepOther, shell.ISyncMgrResolutionHandler_KeepOther, syncmgr/ISyncMgrResolutionHandler::KeepOther
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
 - ISyncMgrResolutionHandler::KeepOther
 - syncmgr/ISyncMgrResolutionHandler::KeepOther
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
 - ISyncMgrResolutionHandler.KeepOther
---

# ISyncMgrResolutionHandler::KeepOther


## -description

Replaces the versions in conflict with a different Shell item that is usually a merged version of the originals.

## -parameters

### -param psiOther [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to the substitute <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>.

### -param pFeedback [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

When this method returns, contains a <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The specified Shell item that replaces the Shell item(s) in conflict may not have been one of those originally in conflict.  It may be a merged copy, or a replacement copy.

The <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value returned in <i>pFeedback</i> determines how the next conflict is resolved. If this method fails, an error message is displayed and the user is asked how to proceed.