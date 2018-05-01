---
UID: NF:searchapi.IOpLockStatus.IsOplockBroken
title: IOpLockStatus::IsOplockBroken method
author: windows-driver-content
description: Checks the status of the opportunistic lock (OpLock) on the item being indexed.
old-location: search\_search_IOpLockStatus_IsOplockBroken.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\isoplockbroken.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IOpLockStatus, IOpLockStatus interface [search], IsOplockBroken method, IOpLockStatus::IsOplockBroken, IsOplockBroken method [search], IsOplockBroken method [search], IOpLockStatus interface, IsOplockBroken,IOpLockStatus.IsOplockBroken, _search_IOpLockStatus_IsOplockBroken, search._search_IOpLockStatus_IsOplockBroken, searchapi/IOpLockStatus::IsOplockBroken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Urlacc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	IOpLockStatus.IsOplockBroken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpLockStatus::IsOplockBroken method


## -description


Checks the status of the opportunistic lock (OpLock) on the item being indexed.


## -parameters




### -param pfIsOplockBroken [out]

Type: <b>BOOL*</b>

Receives a pointer to a <b>BOOL</b> value that indicates whether the OpLock is broken: <b>TRUE</b> if OpLock was taken and then broken, <b>FALSE</b> otherwise (including the case when OpLock was not taken).


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the OpLock is broken, S_FALSE otherwise.




## -remarks



An OpLock is an opportunistic lock that allows the indexer to lock the item when another process isn't accessing it. The indexer releases the item, invalidating or breaking the lock, when another process requests an incompatible access mode. This enables the indexer to run in the background and not impede access to these items by other processes.



