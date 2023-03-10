---
UID: NF:searchapi.IOpLockStatus.IsOplockValid
title: IOpLockStatus::IsOplockValid (searchapi.h)
description: Checks the status of the opportunistic lock (OpLock) on the item being indexed. (IOpLockStatus.IsOplockValid)
helpviewer_keywords: ["IOpLockStatus interface [search]","IsOplockValid method","IOpLockStatus.IsOplockValid","IOpLockStatus::IsOplockValid","IsOplockValid","IsOplockValid method [search]","IsOplockValid method [search]","IOpLockStatus interface","_search_IOpLockStatus_IsOplockValid","search._search_IOpLockStatus_IsOplockValid","searchapi/IOpLockStatus::IsOplockValid"]
old-location: search\_search_IOpLockStatus_IsOplockValid.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\isoplockvalid.htm
ms.date: 12/05/2018
ms.keywords: IOpLockStatus interface [search],IsOplockValid method, IOpLockStatus.IsOplockValid, IOpLockStatus::IsOplockValid, IsOplockValid, IsOplockValid method [search], IsOplockValid method [search],IOpLockStatus interface, _search_IOpLockStatus_IsOplockValid, search._search_IOpLockStatus_IsOplockValid, searchapi/IOpLockStatus::IsOplockValid
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
 - IOpLockStatus::IsOplockValid
 - searchapi/IOpLockStatus::IsOplockValid
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
 - IOpLockStatus.IsOplockValid
---

# IOpLockStatus::IsOplockValid


## -description

Checks the status of the opportunistic lock (OpLock) on the item being indexed.

## -parameters

### -param pfIsOplockValid [out]

Type: <b>BOOL*</b>

Receives a pointer to a <b>BOOL</b> value that indicates whether the OpLock is successfully taken.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An OpLock is an opportunistic lock that allows the indexer to lock the item when another process is not accessing it. The indexer releases the item, invalidating or breaking the lock, when another process requests an incompatible access mode. This enables the indexer to run in the background and not impede access to these items by other processes.

An OpLock is never taken after the underlying <a href="/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object is initialized, and any call to this method yields the same output value on the same object.
