---
UID: NF:syncmgr.ISyncMgrEventStore.GetEvent
title: ISyncMgrEventStore::GetEvent method
author: windows-driver-content
description: Gets a specified event object.
old-location: shell\ISyncMgrEventStore_GetEvent.htm
old-project: shell
ms.assetid: 6800ac62-1fd5-43a4-bd37-831449274a7b
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetEvent method [Windows Shell], GetEvent method [Windows Shell], ISyncMgrEventStore interface, GetEvent,ISyncMgrEventStore.GetEvent, ISyncMgrEventStore, ISyncMgrEventStore interface [Windows Shell], GetEvent method, ISyncMgrEventStore::GetEvent, _shell_ISyncMgrEventStore_GetEvent, shell.ISyncMgrEventStore_GetEvent, syncmgr/ISyncMgrEventStore::GetEvent
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
-	ISyncMgrEventStore.GetEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEventStore::GetEvent method


## -description


Gets a specified event object.


## -parameters




### -param rguidEventID [in]

Type: <b>REFGUID</b>

A reference to event <b>GUID</b>.


### -param ppEvent [out]

Type: <b><a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a>**</b>

The address of <a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



