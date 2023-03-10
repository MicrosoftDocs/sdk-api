---
UID: NF:syncmgr.ISyncMgrEvent.GetLevel
title: ISyncMgrEvent::GetLevel (syncmgr.h)
description: Gets the log level of the event.
helpviewer_keywords: ["GetLevel","GetLevel method [Windows Shell]","GetLevel method [Windows Shell]","ISyncMgrEvent interface","ISyncMgrEvent interface [Windows Shell]","GetLevel method","ISyncMgrEvent.GetLevel","ISyncMgrEvent::GetLevel","_shell_ISyncMgrEvent_GetLevel","shell.ISyncMgrEvent_GetLevel","syncmgr/ISyncMgrEvent::GetLevel"]
old-location: shell\ISyncMgrEvent_GetLevel.htm
tech.root: shell
ms.assetid: 2937dc05-9576-43b4-9fbe-6c151dffcace
ms.date: 12/05/2018
ms.keywords: GetLevel, GetLevel method [Windows Shell], GetLevel method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetLevel method, ISyncMgrEvent.GetLevel, ISyncMgrEvent::GetLevel, _shell_ISyncMgrEvent_GetLevel, shell.ISyncMgrEvent_GetLevel, syncmgr/ISyncMgrEvent::GetLevel
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
 - ISyncMgrEvent::GetLevel
 - syncmgr/ISyncMgrEvent::GetLevel
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
 - ISyncMgrEvent.GetLevel
---

# ISyncMgrEvent::GetLevel


## -description

Gets the log level of the event.

## -parameters

### -param pnLevel [out]

Type: <b><a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_level">SYNCMGR_EVENT_LEVEL</a>*</b>

When this method returns, contains a pointer to a member of the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_event_level">SYNCMGR_EVENT_LEVEL</a> enumeration that indicates the log level.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.