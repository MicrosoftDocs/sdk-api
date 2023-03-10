---
UID: NF:syncmgr.ISyncMgrEvent.GetFlags
title: ISyncMgrEvent::GetFlags (syncmgr.h)
description: Gets event flags.
helpviewer_keywords: ["GetFlags","GetFlags method [Windows Shell]","GetFlags method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetFlags method","ISyncMgrEvent.GetFlags","ISyncMgrEvent::GetFlags","_shell_ISyncMgrEvent_GetFlags","shell.ISyncMgrEvent_GetFlags","syncmgr/ISyncMgrEvent::GetFlags"]
old-location: shell\ISyncMgrEvent_GetFlags.htm
tech.root: shell
ms.assetid: 51651a03-da3d-4b75-97bf-3be1db56054e
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Windows Shell], GetFlags method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetFlags method, ISyncMgrEvent.GetFlags, ISyncMgrEvent::GetFlags, _shell_ISyncMgrEvent_GetFlags, shell.ISyncMgrEvent_GetFlags, syncmgr/ISyncMgrEvent::GetFlags
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
 - ISyncMgrEvent::GetFlags
 - syncmgr/ISyncMgrEvent::GetFlags
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
 - ISyncMgrEvent.GetFlags
---

# ISyncMgrEvent::GetFlags


## -description

Gets event flags.

## -parameters

### -param pnFlags [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_flags">SYNCMGR_EVENT_FLAGS</a>*</b>

When this method returns, contains a pointer to a value that indicates the currently set flags, taken from members of the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_flags">SYNCMGR_EVENT_FLAGS</a> enumeration.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.