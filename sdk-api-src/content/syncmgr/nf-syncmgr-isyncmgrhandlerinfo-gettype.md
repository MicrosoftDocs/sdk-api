---
UID: NF:syncmgr.ISyncMgrHandlerInfo.GetType
title: ISyncMgrHandlerInfo::GetType (syncmgr.h)
description: Gets the handler type for Sync Center.
helpviewer_keywords: ["GetType","GetType method [Windows Shell]","GetType method [Windows Shell]","ISyncMgrHandlerInfo interface","ISyncMgrHandlerInfo interface [Windows Shell]","GetType method","ISyncMgrHandlerInfo.GetType","ISyncMgrHandlerInfo::GetType","_shell_ISyncMgrHandlerInfo_GetType","shell.ISyncMgrHandlerInfo_GetType","syncmgr/ISyncMgrHandlerInfo::GetType"]
old-location: shell\ISyncMgrHandlerInfo_GetType.htm
tech.root: shell
ms.assetid: 466c5bd5-0166-4c0d-801d-a155f20140ce
ms.date: 12/05/2018
ms.keywords: GetType, GetType method [Windows Shell], GetType method [Windows Shell],ISyncMgrHandlerInfo interface, ISyncMgrHandlerInfo interface [Windows Shell],GetType method, ISyncMgrHandlerInfo.GetType, ISyncMgrHandlerInfo::GetType, _shell_ISyncMgrHandlerInfo_GetType, shell.ISyncMgrHandlerInfo_GetType, syncmgr/ISyncMgrHandlerInfo::GetType
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
 - ISyncMgrHandlerInfo::GetType
 - syncmgr/ISyncMgrHandlerInfo::GetType
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
 - ISyncMgrHandlerInfo.GetType
---

# ISyncMgrHandlerInfo::GetType


## -description

Gets the handler type for Sync Center.

## -parameters

### -param pnType [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_type">SYNCMGR_HANDLER_TYPE</a>*</b>

When this method returns, points to a value from the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_type">SYNCMGR_HANDLER_TYPE</a> enumeration that specifies the handler type. If the method fails, this parameter points to <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_type">SYNCMGR_HT_UNSPECIFIED</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>pnType</i> is set to <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_type">SYNCMGR_HT_UNSPECIFIED</a>.

## -remarks

Typically, this value does not change. However, Sync Center calls this method whenever the <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrcontrol-updatehandler">UpdateHandler</a> method is called.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetType(__out SYNCMGR_HANDLER_TYPE *pnType)
{
    *pnType = SYNCMGR_HT_DEVICE;
    return S_OK;

```