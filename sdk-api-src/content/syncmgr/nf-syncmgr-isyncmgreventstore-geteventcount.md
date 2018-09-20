---
UID: NF:syncmgr.ISyncMgrEventStore.GetEventCount
title: ISyncMgrEventStore::GetEventCount
author: windows-sdk-content
description: Gets the event count.
old-location: shell\ISyncMgrEventStore_GetEventCount.htm
tech.root: shell
ms.assetid: 7e8482ed-3cdc-49a3-ad65-237f163e440d
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetEventCount, GetEventCount method [Windows Shell], GetEventCount method [Windows Shell],ISyncMgrEventStore interface, ISyncMgrEventStore interface [Windows Shell],GetEventCount method, ISyncMgrEventStore.GetEventCount, ISyncMgrEventStore::GetEventCount, _shell_ISyncMgrEventStore_GetEventCount, shell.ISyncMgrEventStore_GetEventCount, syncmgr/ISyncMgrEventStore::GetEventCount
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrEventStore.GetEventCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



