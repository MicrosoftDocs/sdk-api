---
UID: NF:syncmgr.ISyncMgrHandler.GetPolicies
title: ISyncMgrHandler::GetPolicies (syncmgr.h)
author: windows-sdk-content
description: Gets a set of flags describing the policies set by the handler.
old-location: shell\ISyncMgrHandler_GetPolicies.htm
tech.root: shell
ms.assetid: ff30441a-43bb-4f30-af04-4d2056b8dfb0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPolicies, GetPolicies method [Windows Shell], GetPolicies method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetPolicies method, ISyncMgrHandler.GetPolicies, ISyncMgrHandler::GetPolicies, _shell_ISyncMgrHandler_GetPolicies, shell.ISyncMgrHandler_GetPolicies, syncmgr/ISyncMgrHandler::GetPolicies
ms.topic: method
f1_keywords: 
 - "syncmgr/ISyncMgrHandler.GetPolicies"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrHandler.GetPolicies
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrHandler::GetPolicies


## -description


Gets a set of flags describing the policies set by the handler.


## -parameters




### -param pmPolicies [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HANDLER_POLICIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HANDLER_POLICIES</a> enumeration that define the handler's policies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A policy is an action that is usually supported but can be disabled by a group policy.

This method is called by Sync Center in response to a call to <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> or <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandlercollection">UpdateHandlerCollection</a>.


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




