---
UID: NF:syncmgr.ISyncMgrEvent.GetItemID
title: ISyncMgrEvent::GetItemID (syncmgr.h)
description: Gets the ID of the item for which the event was logged.
helpviewer_keywords: ["GetItemID","GetItemID method [Windows Shell]","GetItemID method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetItemID method","ISyncMgrEvent.GetItemID","ISyncMgrEvent::GetItemID","_shell_ISyncMgrEvent_GetItemID","shell.ISyncMgrEvent_GetItemID","syncmgr/ISyncMgrEvent::GetItemID"]
old-location: shell\ISyncMgrEvent_GetItemID.htm
tech.root: shell
ms.assetid: 243f84eb-ad0b-44ac-bf61-53bb8b6e5af5
ms.date: 12/05/2018
ms.keywords: GetItemID, GetItemID method [Windows Shell], GetItemID method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetItemID method, ISyncMgrEvent.GetItemID, ISyncMgrEvent::GetItemID, _shell_ISyncMgrEvent_GetItemID, shell.ISyncMgrEvent_GetItemID, syncmgr/ISyncMgrEvent::GetItemID
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
 - ISyncMgrEvent::GetItemID
 - syncmgr/ISyncMgrEvent::GetItemID
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
 - ISyncMgrEvent.GetItemID
---

# ISyncMgrEvent::GetItemID


## -description

Gets the ID of the item for which the event was logged.

## -parameters

### -param ppszItemID [out]

Type: <b>LPWSTR*</b>

Contains a pointer to an item ID as a Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The item ID can have a maximum length of MAX_SYNCMGR_ID, including the terminating null character. The event is expected to allocate the string buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.