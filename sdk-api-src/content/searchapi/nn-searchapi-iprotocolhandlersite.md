---
UID: NN:searchapi.IProtocolHandlerSite
title: IProtocolHandlerSite (searchapi.h)
description: Provides methods for a protocol handler's IUrlAccessor object to query the Filter Daemon for the appropriate filter for the URL item.
helpviewer_keywords: ["IProtocolHandlerSite","IProtocolHandlerSite interface [search]","IProtocolHandlerSite interface [search]","described","_search_IProtocolHandlerSite","search._search_IProtocolHandlerSite","searchapi/IProtocolHandlerSite"]
old-location: search\_search_IProtocolHandlerSite.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\protocolhandlers\iprotocolhandlersite\iprotocolhandlersite.htm
ms.date: 12/05/2018
ms.keywords: IProtocolHandlerSite, IProtocolHandlerSite interface [search], IProtocolHandlerSite interface [search],described, _search_IProtocolHandlerSite, search._search_IProtocolHandlerSite, searchapi/IProtocolHandlerSite
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Srchprth.idl
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
 - IProtocolHandlerSite
 - searchapi/IProtocolHandlerSite
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
 - IProtocolHandlerSite
---

# IProtocolHandlerSite interface


## -description

Provides methods for a protocol handler's <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor">IUrlAccessor</a> object to query the Filter Daemon for the appropriate filter for the URL item.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProtocolHandlerSite</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProtocolHandlerSite</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProtocolHandlerSite</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iprotocolhandlersite-getfilter">GetFilter</a>
</td>
<td align="left" width="63%">
Retrieves the appropriate <a href="https://docs.microsoft.com/windows/desktop/api/filter/nn-filter-ifilter">IFilter</a>according to the supplied parameters.     
        

</td>
</tr>
</table>

## -remarks

When a protocol handler encounters items with embedded documents, the protocol handler requests additional filters from the Filter Daemon by calling the <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-iprotocolhandlersite-getfilter">IProtocolHandlerSite::GetFilter</a> method.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>

