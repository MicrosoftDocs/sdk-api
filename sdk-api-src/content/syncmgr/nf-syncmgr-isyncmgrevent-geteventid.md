---
UID: NF:syncmgr.ISyncMgrEvent.GetEventID
title: ISyncMgrEvent::GetEventID
author: windows-driver-content
description: Gets the event ID.
old-location: shell\ISyncMgrEvent_GetEventID.htm
old-project: shell
ms.assetid: 2951a015-b365-468b-a143-1b807885a99a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetEventID, GetEventID method [Windows Shell], GetEventID method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetEventID method, ISyncMgrEvent.GetEventID, ISyncMgrEvent::GetEventID, _shell_ISyncMgrEvent_GetEventID, shell.ISyncMgrEvent_GetEventID, syncmgr/ISyncMgrEvent::GetEventID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrEvent.GetEventID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



