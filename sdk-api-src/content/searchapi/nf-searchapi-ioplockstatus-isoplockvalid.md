---
UID: NF:searchapi.IOpLockStatus.IsOplockValid
title: IOpLockStatus::IsOplockValid
author: windows-sdk-content
description: Checks the status of the opportunistic lock (OpLock) on the item being indexed.
old-location: search\_search_IOpLockStatus_IsOplockValid.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\isoplockvalid.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOpLockStatus interface [search],IsOplockValid method, IOpLockStatus.IsOplockValid, IOpLockStatus::IsOplockValid, IsOplockValid, IsOplockValid method [search], IsOplockValid method [search],IOpLockStatus interface, _search_IOpLockStatus_IsOplockValid, search._search_IOpLockStatus_IsOplockValid, searchapi/IOpLockStatus::IsOplockValid
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - IOpLockStatus.IsOplockValid
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An OpLock is an opportunistic lock that allows the indexer to lock the item when another process is not accessing it. The indexer releases the item, invalidating or breaking the lock, when another process requests an incompatible access mode. This enables the indexer to run in the background and not impede access to these items by other processes.

An OpLock is never taken after the underlying <a href="https://msdn.microsoft.com/1e6272e7-d9bc-4372-8feb-f96626b88903">IUrlAccessor</a> object is initialized, and any call to this method yields the same output value on the same object.
            



