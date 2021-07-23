---
UID: NF:syncmgr.ISyncMgrEvent.GetName
title: ISyncMgrEvent::GetName (syncmgr.h)
description: Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event.
helpviewer_keywords: ["GetName","GetName method [Windows Shell]","GetName method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetName method","ISyncMgrEvent.GetName","ISyncMgrEvent::GetName","_shell_ISyncMgrEvent_GetName","shell.ISyncMgrEvent_GetName","syncmgr/ISyncMgrEvent::GetName"]
old-location: shell\ISyncMgrEvent_GetName.htm
tech.root: shell
ms.assetid: d533ab62-f6b2-4be9-ac58-98250d99a8c3
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Windows Shell], GetName method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetName method, ISyncMgrEvent.GetName, ISyncMgrEvent::GetName, _shell_ISyncMgrEvent_GetName, shell.ISyncMgrEvent_GetName, syncmgr/ISyncMgrEvent::GetName
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
 - ISyncMgrEvent::GetName
 - syncmgr/ISyncMgrEvent::GetName
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
 - ISyncMgrEvent.GetName
---

# ISyncMgrEvent::GetName


## -description

Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event.

## -parameters

### -param ppszName [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a name as a Unicode string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The event is expected to allocate the string buffer using <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.