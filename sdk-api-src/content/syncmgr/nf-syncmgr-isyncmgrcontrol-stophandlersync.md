---
UID: NF:syncmgr.ISyncMgrControl.StopHandlerSync
title: ISyncMgrControl::StopHandlerSync (syncmgr.h)
description: Stops the synchronization of a specified handler.
helpviewer_keywords: ["ISyncMgrControl interface [Windows Shell]","StopHandlerSync method","ISyncMgrControl.StopHandlerSync","ISyncMgrControl::StopHandlerSync","StopHandlerSync","StopHandlerSync method [Windows Shell]","StopHandlerSync method [Windows Shell]","ISyncMgrControl interface","_shell_ISyncMgrControl_StopHandlerSync","shell.ISyncMgrControl_StopHandlerSync","syncmgr/ISyncMgrControl::StopHandlerSync"]
old-location: shell\ISyncMgrControl_StopHandlerSync.htm
tech.root: shell
ms.assetid: 0a1ba08a-8765-49b5-be71-373af76375f8
ms.date: 12/05/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],StopHandlerSync method, ISyncMgrControl.StopHandlerSync, ISyncMgrControl::StopHandlerSync, StopHandlerSync, StopHandlerSync method [Windows Shell], StopHandlerSync method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_StopHandlerSync, shell.ISyncMgrControl_StopHandlerSync, syncmgr/ISyncMgrControl::StopHandlerSync
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
 - ISyncMgrControl::StopHandlerSync
 - syncmgr/ISyncMgrControl::StopHandlerSync
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
 - ISyncMgrControl.StopHandlerSync
---

# ISyncMgrControl::StopHandlerSync


## -description

Stops the synchronization of a specified handler.

## -parameters

### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

