---
UID: NF:syncmgr.ISyncMgrHandler.GetPolicies
title: ISyncMgrHandler::GetPolicies (syncmgr.h)
description: Gets a set of flags describing the policies set by the handler.
helpviewer_keywords: ["GetPolicies","GetPolicies method [Windows Shell]","GetPolicies method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","GetPolicies method","ISyncMgrHandler.GetPolicies","ISyncMgrHandler::GetPolicies","_shell_ISyncMgrHandler_GetPolicies","shell.ISyncMgrHandler_GetPolicies","syncmgr/ISyncMgrHandler::GetPolicies"]
old-location: shell\ISyncMgrHandler_GetPolicies.htm
tech.root: shell
ms.assetid: ff30441a-43bb-4f30-af04-4d2056b8dfb0
ms.date: 12/05/2018
ms.keywords: GetPolicies, GetPolicies method [Windows Shell], GetPolicies method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetPolicies method, ISyncMgrHandler.GetPolicies, ISyncMgrHandler::GetPolicies, _shell_ISyncMgrHandler_GetPolicies, shell.ISyncMgrHandler_GetPolicies, syncmgr/ISyncMgrHandler::GetPolicies
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
 - ISyncMgrHandler::GetPolicies
 - syncmgr/ISyncMgrHandler::GetPolicies
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
 - ISyncMgrHandler.GetPolicies
---

# ISyncMgrHandler::GetPolicies


## -description

Gets a set of flags describing the policies set by the handler.

## -parameters

### -param pmPolicies [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HANDLER_POLICIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HANDLER_POLICIES</a> enumeration that define the handler's policies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A policy is an action that is usually supported but can be disabled by a group policy.

This method is called by Sync Center in response to a call to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> or <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandlercollection">UpdateHandlerCollection</a>.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetPolicies(
                             __out SYNCMGR_HANDLER_POLICIES *pmPolicies)
{
    *pmPolicies = SYNCMGR_HPM_NONE;
    return S_OK;
}

```