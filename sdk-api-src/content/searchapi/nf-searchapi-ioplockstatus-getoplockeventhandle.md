---
UID: NF:searchapi.IOpLockStatus.GetOplockEventHandle
title: IOpLockStatus::GetOplockEventHandle (searchapi.h)
description: Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying IUrlAccessor object.
helpviewer_keywords: ["GetOplockEventHandle","GetOplockEventHandle method [search]","GetOplockEventHandle method [search]","IOpLockStatus interface","IOpLockStatus interface [search]","GetOplockEventHandle method","IOpLockStatus.GetOplockEventHandle","IOpLockStatus::GetOplockEventHandle","_search_IOpLockStatus_GetOplockEventHandle","search._search_IOpLockStatus_GetOplockEventHandle","searchapi/IOpLockStatus::GetOplockEventHandle"]
old-location: search\_search_IOpLockStatus_GetOplockEventHandle.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\getoplockeventhandle.htm
ms.date: 12/05/2018
ms.keywords: GetOplockEventHandle, GetOplockEventHandle method [search], GetOplockEventHandle method [search],IOpLockStatus interface, IOpLockStatus interface [search],GetOplockEventHandle method, IOpLockStatus.GetOplockEventHandle, IOpLockStatus::GetOplockEventHandle, _search_IOpLockStatus_GetOplockEventHandle, search._search_IOpLockStatus_GetOplockEventHandle, searchapi/IOpLockStatus::GetOplockEventHandle
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IOpLockStatus::GetOplockEventHandle
 - searchapi/IOpLockStatus::GetOplockEventHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IOpLockStatus.GetOplockEventHandle
---

# IOpLockStatus::GetOplockEventHandle


## -description

Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object.

## -parameters

### -param phOplockEv [out]

Type: <b>HANDLE*</b>

Receives a pointer to the handle of the event associated with the OpLock, or <b>NULL</b> if no OpLock was taken.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.