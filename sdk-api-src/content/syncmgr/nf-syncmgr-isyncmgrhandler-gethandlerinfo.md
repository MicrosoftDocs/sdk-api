---
UID: NF:syncmgr.ISyncMgrHandler.GetHandlerInfo
title: ISyncMgrHandler::GetHandlerInfo (syncmgr.h)
description: Gets properties that describe the handler.
helpviewer_keywords: ["GetHandlerInfo","GetHandlerInfo method [Windows Shell]","GetHandlerInfo method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","GetHandlerInfo method","ISyncMgrHandler.GetHandlerInfo","ISyncMgrHandler::GetHandlerInfo","_shell_ISyncMgrHandler_GetHandlerInfo","shell.ISyncMgrHandler_GetHandlerInfo","syncmgr/ISyncMgrHandler::GetHandlerInfo"]
old-location: shell\ISyncMgrHandler_GetHandlerInfo.htm
tech.root: shell
ms.assetid: 078f7cee-fb75-4b8b-8c90-720c26d1f361
ms.date: 12/05/2018
ms.keywords: GetHandlerInfo, GetHandlerInfo method [Windows Shell], GetHandlerInfo method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetHandlerInfo method, ISyncMgrHandler.GetHandlerInfo, ISyncMgrHandler::GetHandlerInfo, _shell_ISyncMgrHandler_GetHandlerInfo, shell.ISyncMgrHandler_GetHandlerInfo, syncmgr/ISyncMgrHandler::GetHandlerInfo
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
 - ISyncMgrHandler::GetHandlerInfo
 - syncmgr/ISyncMgrHandler::GetHandlerInfo
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
 - ISyncMgrHandler.GetHandlerInfo
---

# ISyncMgrHandler::GetHandlerInfo


## -description

Gets properties that describe the handler.

## -parameters

### -param ppHandlerInfo [out]

Type: <b><a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandlerinfo">ISyncMgrHandlerInfo</a>**</b>

When this method returns, contains the address of a pointer to an instance of the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandlerinfo">ISyncMgrHandlerInfo</a> interface that provides access to the handler properties.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If this method fails, the handler is still shown in the Sync Center folder and Sync Center continues to invoke it, but default values are used for all properties.

<b>ISyncMgrHandler::GetHandlerInfo</b>, together with <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getname">ISyncMgrHandler::GetName</a>, replaces the older <a href="/windows/desktop/api/mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo">GetHandlerInfo</a>.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetHandlerInfo(
                             __out ISyncMgrHandlerInfo **ppHandlerInfo)
{
    *ppHandlerInfo = NULL;
    HRESULT hr = QueryInterface(IID_ISyncMgrHandlerInfo, 
                                (void **) ppHandlerInfo);
    return hr;
}

```