---
UID: NF:syncmgr.ISyncMgrEvent.GetDescription
title: ISyncMgrEvent::GetDescription (syncmgr.h)
description: Gets the event description.
helpviewer_keywords: ["GetDescription","GetDescription method [Windows Shell]","GetDescription method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetDescription method","ISyncMgrEvent.GetDescription","ISyncMgrEvent::GetDescription","_shell_ISyncMgrEvent_GetDescription","shell.ISyncMgrEvent_GetDescription","syncmgr/ISyncMgrEvent::GetDescription"]
old-location: shell\ISyncMgrEvent_GetDescription.htm
tech.root: shell
ms.assetid: 3ec45cf6-d282-4df9-bd4a-b5d75df69ff4
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Windows Shell], GetDescription method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetDescription method, ISyncMgrEvent.GetDescription, ISyncMgrEvent::GetDescription, _shell_ISyncMgrEvent_GetDescription, shell.ISyncMgrEvent_GetDescription, syncmgr/ISyncMgrEvent::GetDescription
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
 - ISyncMgrEvent::GetDescription
 - syncmgr/ISyncMgrEvent::GetDescription
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
 - ISyncMgrEvent.GetDescription
---

# ISyncMgrEvent::GetDescription


## -description

Gets the event description.

## -parameters

### -param ppszDescription [out]

Type: <b>LPWSTR*</b>

When this method returns, contains the address of a pointer to a null-terminated Unicode buffer that contains the description.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

