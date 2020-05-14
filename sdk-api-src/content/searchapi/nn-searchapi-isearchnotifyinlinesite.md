---
UID: NN:searchapi.ISearchNotifyInlineSite
title: ISearchNotifyInlineSite (searchapi.h)
description: Provides methods the Search service uses to send updates on catalog and index status to notification providers.helpviewer_keywords: ["ISearchNotifyInlineSite","ISearchNotifyInlineSite interface [search]","ISearchNotifyInlineSite interface [search]","described","_search_ISearchNotifyInlineSite","search._search_ISearchNotifyInlineSite","searchapi/ISearchNotifyInlineSite"]
old-location: search\_search_ISearchNotifyInlineSite.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\notifications\isearchnotifyinlinesite\isearchnotifyinlinesite.htm
ms.date: 12/05/2018
ms.keywords: ISearchNotifyInlineSite, ISearchNotifyInlineSite interface [search], ISearchNotifyInlineSite interface [search],described, _search_ISearchNotifyInlineSite, search._search_ISearchNotifyInlineSite, searchapi/ISearchNotifyInlineSite
f1_keywords:
- searchapi/ISearchNotifyInlineSite
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
req.idl: Srchntfyinlinesite.idl
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
- ISearchNotifyInlineSite
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchNotifyInlineSite interface


## -description


Provides methods the Search service uses to send updates on catalog and index status to notification providers.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchNotifyInlineSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchNotifyInlineSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchNotifyInlineSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchnotifyinlinesite-oncatalogstatuschange">OnCatalogStatusChange</a>
</td>
<td align="left" width="63%">
Called by the search service to notify a client when the status of the catalog changes.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchnotifyinlinesite-onitemindexedstatuschange">OnItemIndexedStatusChange</a>
</td>
<td align="left" width="63%">
Called by the search service to notify the client when the status of a particular document or item changes.
        

</td>
</tr>
</table> 


## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-notifyingofchanges">Notifying the Index of Changes</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>
 

 

