---
UID: NF:searchapi.IOpLockStatus.GetOplockEventHandle
title: IOpLockStatus::GetOplockEventHandle
author: windows-sdk-content
description: Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying IUrlAccessor object.
old-location: search\_search_IOpLockStatus_GetOplockEventHandle.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\getoplockeventhandle.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetOplockEventHandle, GetOplockEventHandle method [search], GetOplockEventHandle method [search],IOpLockStatus interface, IOpLockStatus interface [search],GetOplockEventHandle method, IOpLockStatus.GetOplockEventHandle, IOpLockStatus::GetOplockEventHandle, _search_IOpLockStatus_GetOplockEventHandle, search._search_IOpLockStatus_GetOplockEventHandle, searchapi/IOpLockStatus::GetOplockEventHandle
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IOpLockStatus.GetOplockEventHandle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOpLockStatus::GetOplockEventHandle


## -description


Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying <a href="https://msdn.microsoft.com/library/Bb231426(v=VS.85).aspx">IUrlAccessor</a> object.


## -parameters




### -param phOplockEv [out]

Type: <b>HANDLE*</b>

Receives a pointer to the handle of the event associated with the OpLock, or <b>NULL</b> if no OpLock was taken.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



