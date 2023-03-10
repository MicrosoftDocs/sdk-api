---
UID: NF:syncmgr.ISyncMgrEvent.GetHandlerID
title: ISyncMgrEvent::GetHandlerID (syncmgr.h)
description: Gets the ID of the handler for which the event was logged.
helpviewer_keywords: ["GetHandlerID","GetHandlerID method [Windows Shell]","GetHandlerID method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetHandlerID method","ISyncMgrEvent.GetHandlerID","ISyncMgrEvent::GetHandlerID","_shell_ISyncMgrEvent_GetHandlerID","shell.ISyncMgrEvent_GetHandlerID","syncmgr/ISyncMgrEvent::GetHandlerID"]
old-location: shell\ISyncMgrEvent_GetHandlerID.htm
tech.root: shell
ms.assetid: b2f3bcbf-f14d-41ce-b4fc-3f491465ce84
ms.date: 12/05/2018
ms.keywords: GetHandlerID, GetHandlerID method [Windows Shell], GetHandlerID method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetHandlerID method, ISyncMgrEvent.GetHandlerID, ISyncMgrEvent::GetHandlerID, _shell_ISyncMgrEvent_GetHandlerID, shell.ISyncMgrEvent_GetHandlerID, syncmgr/ISyncMgrEvent::GetHandlerID
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
 - ISyncMgrEvent::GetHandlerID
 - syncmgr/ISyncMgrEvent::GetHandlerID
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
 - ISyncMgrEvent.GetHandlerID
---

# ISyncMgrEvent::GetHandlerID


## -description

Gets the ID of the handler for which the event was logged.

## -parameters

### -param ppszHandlerID [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a handler ID as a Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The handler ID can have a maximum length of MAX_SYNCMGR_ID, including the terminating null character. The event is expected to allocate the string buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.