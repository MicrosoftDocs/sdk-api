---
UID: NF:syncmgr.ISyncMgrResolutionHandler.KeepRecent
title: ISyncMgrResolutionHandler::KeepRecent (syncmgr.h)
description: Keeps the more recent copy.
helpviewer_keywords: ["ISyncMgrResolutionHandler interface [Windows Shell]","KeepRecent method","ISyncMgrResolutionHandler.KeepRecent","ISyncMgrResolutionHandler::KeepRecent","KeepRecent","KeepRecent method [Windows Shell]","KeepRecent method [Windows Shell]","ISyncMgrResolutionHandler interface","_shell_ISyncMgrResolutionHandler_KeepRecent","shell.ISyncMgrResolutionHandler_KeepRecent","syncmgr/ISyncMgrResolutionHandler::KeepRecent"]
old-location: shell\ISyncMgrResolutionHandler_KeepRecent.htm
tech.root: shell
ms.assetid: a2327234-4a8d-42b4-aa62-f5c286e3c24b
ms.date: 12/05/2018
ms.keywords: ISyncMgrResolutionHandler interface [Windows Shell],KeepRecent method, ISyncMgrResolutionHandler.KeepRecent, ISyncMgrResolutionHandler::KeepRecent, KeepRecent, KeepRecent method [Windows Shell], KeepRecent method [Windows Shell],ISyncMgrResolutionHandler interface, _shell_ISyncMgrResolutionHandler_KeepRecent, shell.ISyncMgrResolutionHandler_KeepRecent, syncmgr/ISyncMgrResolutionHandler::KeepRecent
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
 - ISyncMgrResolutionHandler::KeepRecent
 - syncmgr/ISyncMgrResolutionHandler::KeepRecent
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
 - ISyncMgrResolutionHandler.KeepRecent
---

# ISyncMgrResolutionHandler::KeepRecent


## -description

Keeps the more recent copy.

## -parameters

### -param pFeedback [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a>*</b>

When this method returns, contains a <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_resolution_feedback">SYNCMGR_RESOLUTION_FEEDBACK</a> value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.