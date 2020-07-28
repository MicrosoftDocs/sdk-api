---
UID: NN:searchapi.IOpLockStatus
title: IOpLockStatus (searchapi.h)
description: Provides methods to check the opportunistic lock that is used by Microsoft Windows Desktop Search (WDS) on items while indexing.
helpviewer_keywords: ["IOpLockStatus","IOpLockStatus interface [search]","IOpLockStatus interface [search]","described","_search_IOpLockStatus","search._search_IOpLockStatus","searchapi/IOpLockStatus"]
old-location: search\_search_IOpLockStatus.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\ioplockstatus\ioplockstatus.htm
ms.date: 12/05/2018
ms.keywords: IOpLockStatus, IOpLockStatus interface [search], IOpLockStatus interface [search],described, _search_IOpLockStatus, search._search_IOpLockStatus, searchapi/IOpLockStatus
f1_keywords:
- searchapi/IOpLockStatus
dev_langs:
- c++
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
- IOpLockStatus
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IOpLockStatus interface


## -description


Provides methods to check the opportunistic lock that is used by Microsoft Windows Desktop Search (WDS) on items while indexing. If another process locks the file in an incompatible manner, WDS will lose its lock and allow the other process to have the file. This mechanism allows WDS to run in the background. Consequently, WDS needs to check its locks to ensure another process has not taken precedence while WDS indexes the item. 



A third-party <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object can implement this interface if the underlying data store provides a mechanism to track concurrent access to items. If this interface is exposed by <b>IUrlAccessor</b>, WDS will check the <b>IOpLockStatus</b> while indexing items from that store. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpLockStatus</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpLockStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpLockStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ioplockstatus-getoplockeventhandle">GetOplockEventHandle</a>
</td>
<td align="left" width="63%">
Gets the event handle of the opportunistic lock (OpLock). The event object is set to the signaled state when the OpLock is broken, enabling the indexer to stop all operations on the underlying <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ioplockstatus-isoplockbroken">IsOplockBroken</a>
</td>
<td align="left" width="63%">
Checks the status of the opportunistic lock (OpLock) on the item being indexed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-ioplockstatus-isoplockvalid">IsOplockValid</a>
</td>
<td align="left" width="63%">
Checks the status of the opportunistic lock (OpLock) on the item being indexed.

</td>
</tr>
</table> 

