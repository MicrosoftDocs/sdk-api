---
UID: NF:syncmgr.ISyncMgrHandler.GetCapabilities
title: ISyncMgrHandler::GetCapabilities (syncmgr.h)
description: Gets a set of flags describing the handler's defined capabilities.
helpviewer_keywords: ["GetCapabilities","GetCapabilities method [Windows Shell]","GetCapabilities method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","GetCapabilities method","ISyncMgrHandler.GetCapabilities","ISyncMgrHandler::GetCapabilities","_shell_ISyncMgrHandler_GetCapabilities","shell.ISyncMgrHandler_GetCapabilities","syncmgr/ISyncMgrHandler::GetCapabilities"]
old-location: shell\ISyncMgrHandler_GetCapabilities.htm
tech.root: shell
ms.assetid: 3eb43984-f284-4df9-934b-1dd2f0e62e26
ms.date: 12/05/2018
ms.keywords: GetCapabilities, GetCapabilities method [Windows Shell], GetCapabilities method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetCapabilities method, ISyncMgrHandler.GetCapabilities, ISyncMgrHandler::GetCapabilities, _shell_ISyncMgrHandler_GetCapabilities, shell.ISyncMgrHandler_GetCapabilities, syncmgr/ISyncMgrHandler::GetCapabilities
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
 - ISyncMgrHandler::GetCapabilities
 - syncmgr/ISyncMgrHandler::GetCapabilities
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
 - ISyncMgrHandler.GetCapabilities
---

# ISyncMgrHandler::GetCapabilities


## -description

Gets a set of flags describing the handler's defined capabilities.

## -parameters

### -param pmCapabilities [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HANDLER_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HANDLER_CAPABILITIES</a> enumeration that defines the capabilities of the handler. Compare against <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_VALID_MASK</a> to verify a valid value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is called by Sync Center in response to a call to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandlercollection">UpdateHandlerCollection</a>.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetCapabilities(
                             __out SYNCMGR_HANDLER_CAPABILITIES *pmCapabilities)
{
    *pmCapabilities = SYNCMGR_HCM_EVENT_STORE
                    | SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE;
    return S_OK;
}

```