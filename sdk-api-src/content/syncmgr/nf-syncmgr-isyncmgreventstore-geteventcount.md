---
UID: NF:syncmgr.ISyncMgrEventStore.GetEventCount
title: ISyncMgrEventStore::GetEventCount (syncmgr.h)
description: Gets the event count.
helpviewer_keywords: ["GetEventCount","GetEventCount method [Windows Shell]","GetEventCount method [Windows Shell]","ISyncMgrEventStore interface","ISyncMgrEventStore interface [Windows Shell]","GetEventCount method","ISyncMgrEventStore.GetEventCount","ISyncMgrEventStore::GetEventCount","_shell_ISyncMgrEventStore_GetEventCount","shell.ISyncMgrEventStore_GetEventCount","syncmgr/ISyncMgrEventStore::GetEventCount"]
old-location: shell\ISyncMgrEventStore_GetEventCount.htm
tech.root: shell
ms.assetid: 7e8482ed-3cdc-49a3-ad65-237f163e440d
ms.date: 12/05/2018
ms.keywords: GetEventCount, GetEventCount method [Windows Shell], GetEventCount method [Windows Shell],ISyncMgrEventStore interface, ISyncMgrEventStore interface [Windows Shell],GetEventCount method, ISyncMgrEventStore.GetEventCount, ISyncMgrEventStore::GetEventCount, _shell_ISyncMgrEventStore_GetEventCount, shell.ISyncMgrEventStore_GetEventCount, syncmgr/ISyncMgrEventStore::GetEventCount
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
 - ISyncMgrEventStore::GetEventCount
 - syncmgr/ISyncMgrEventStore::GetEventCount
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
 - ISyncMgrEventStore.GetEventCount
---

# ISyncMgrEventStore::GetEventCount


## -description

Gets the event count.

## -parameters

### -param pcEvents [out]

Type: <b>ULONG*</b>

A pointer to event count value.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

