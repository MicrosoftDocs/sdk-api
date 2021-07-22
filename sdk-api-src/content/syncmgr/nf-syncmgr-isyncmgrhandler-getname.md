---
UID: NF:syncmgr.ISyncMgrHandler.GetName
title: ISyncMgrHandler::GetName (syncmgr.h)
description: Gets the display name of the handler.
helpviewer_keywords: ["GetName","GetName method [Windows Shell]","GetName method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","GetName method","ISyncMgrHandler.GetName","ISyncMgrHandler::GetName","_shell_ISyncMgrHandler_GetName","shell.ISyncMgrHandler_GetName","syncmgr/ISyncMgrHandler::GetName"]
old-location: shell\ISyncMgrHandler_GetName.htm
tech.root: shell
ms.assetid: 2d981cf9-6c0a-4bca-b088-06eb1c820fb3
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Shell], GetName method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetName method, ISyncMgrHandler.GetName, ISyncMgrHandler::GetName, _shell_ISyncMgrHandler_GetName, shell.ISyncMgrHandler_GetName, syncmgr/ISyncMgrHandler::GetName
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
 - ISyncMgrHandler::GetName
 - syncmgr/ISyncMgrHandler::GetName
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
 - ISyncMgrHandler.GetName
---

# ISyncMgrHandler::GetName


## -description

Gets the display name of the handler.

## -parameters

### -param ppszName [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a <b>null</b>-terminated buffer that receives the handler name. The name can be of maximum length MAX_SYNCMGR_NAME, including the terminating <b>null</b> character. If the name exceeds that length, it is truncated.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The handler name is accessed as the System.DisplayName (PKEY_DisplayName) property in the Sync Center folder.

Sync Center calls this method any time that <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandlercollection">UpdateHandlerCollection</a> is called. If <b>ISyncMgrHandler::GetName</b> fails or returns an empty string, the handler is not shown in the Sync Center folder and Sync Center will not attempt to invoke it.

It is the responsibility of the handler to allocate the string buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. Sync Center deallocates the buffer through <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

<b>ISyncMgrHandler::GetName</b> replaces the use of <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo">GetHandlerInfo</a> to retrieve the handler name.