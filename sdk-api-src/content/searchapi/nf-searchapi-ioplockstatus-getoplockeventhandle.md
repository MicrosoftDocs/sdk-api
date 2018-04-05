---
UID: NF:searchapi.IOpLockStatus.GetOplockEventHandle
title: IOpLockStatus::GetOplockEventHandle method
author: windows-driver-content
description: Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying IUrlAccessor object.
old-location: search\_search_IOpLockStatus_GetOplockEventHandle.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\getoplockeventhandle.htm
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetOplockEventHandle method [search], GetOplockEventHandle method [search], IOpLockStatus interface, GetOplockEventHandle,IOpLockStatus.GetOplockEventHandle, IOpLockStatus, IOpLockStatus interface [search], GetOplockEventHandle method, IOpLockStatus::GetOplockEventHandle, _search_IOpLockStatus_GetOplockEventHandle, search._search_IOpLockStatus_GetOplockEventHandle, searchapi/IOpLockStatus::GetOplockEventHandle
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
-	IOpLockStatus.GetOplockEventHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IOpLockStatus::GetOplockEventHandle method


## -description


Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object.


## -parameters




### -param phOplockEv [out]

Type: <b>HANDLE*</b>

Receives a pointer to the handle of the event associated with the OpLock, or <b>NULL</b> if no OpLock was taken.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



