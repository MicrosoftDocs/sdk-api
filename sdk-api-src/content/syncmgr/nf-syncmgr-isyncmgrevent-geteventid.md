---
UID: NF:syncmgr.ISyncMgrEvent.GetEventID
title: ISyncMgrEvent::GetEventID (syncmgr.h)
description: Gets the event ID.
helpviewer_keywords: ["GetEventID","GetEventID method [Windows Shell]","GetEventID method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetEventID method","ISyncMgrEvent.GetEventID","ISyncMgrEvent::GetEventID","_shell_ISyncMgrEvent_GetEventID","shell.ISyncMgrEvent_GetEventID","syncmgr/ISyncMgrEvent::GetEventID"]
old-location: shell\ISyncMgrEvent_GetEventID.htm
tech.root: shell
ms.assetid: 2951a015-b365-468b-a143-1b807885a99a
ms.date: 12/05/2018
ms.keywords: GetEventID, GetEventID method [Windows Shell], GetEventID method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetEventID method, ISyncMgrEvent.GetEventID, ISyncMgrEvent::GetEventID, _shell_ISyncMgrEvent_GetEventID, shell.ISyncMgrEvent_GetEventID, syncmgr/ISyncMgrEvent::GetEventID
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
 - ISyncMgrEvent::GetEventID
 - syncmgr/ISyncMgrEvent::GetEventID
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
 - ISyncMgrEvent.GetEventID
---

# ISyncMgrEvent::GetEventID


## -description

Gets the event ID.

## -parameters

### -param pguidEventID [out]

Type: <b>GUID*</b>

When this method returns, contains a pointer to an event ID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

