---
UID: NN:searchapi.ISearchCatalogManager
title: ISearchCatalogManager (searchapi.h)
description: Provides methods to manage a search catalog for purposes such as re-indexing or setting timeouts.
helpviewer_keywords: ["ISearchCatalogManager","ISearchCatalogManager interface [search]","ISearchCatalogManager interface [search]","described","_search_ISearchCatalogManager","search._search_ISearchCatalogManager","searchapi/ISearchCatalogManager"]
old-location: search\_search_ISearchCatalogManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\isearchcatalogmanager.htm
ms.date: 12/05/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], ISearchCatalogManager interface [search],described, _search_ISearchCatalogManager, search._search_ISearchCatalogManager, searchapi/ISearchCatalogManager
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchcatalog.idl
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
 - ISearchCatalogManager
 - searchapi/ISearchCatalogManager
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
 - ISearchCatalogManager
---

# ISearchCatalogManager interface


## -description

Provides methods to manage a search catalog for purposes such as re-indexing or setting timeouts.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCatalogManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchCatalogManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCatalogManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-enumerateexcludedextensions">EnumerateExcludedExtensions</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-get_connecttimeout">get_ConnectTimeout</a>
</td>
<td align="left" width="63%">
Gets the connection time-out value for connecting to a store for indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-get_datatimeout">get_DataTimeout</a>
</td>
<td align="left" width="63%">
Gets the data time-out value, in seconds, for data transactions between the indexer and the search  filter host. This value is contained in a <a href="/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> structure. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-get_diacriticsensitivity">get_DiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the name of the current catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getcatalogstatus">GetCatalogStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager">GetCrawlScopeManager</a>
</td>
<td align="left" width="63%">
Gets an <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager">ISearchCrawlScopeManager</a> interface for this search catalog.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getitemschangedsink">GetItemsChangedSink</a>
</td>
<td align="left" width="63%">
Gets the change notification sink interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getparameter">GetParameter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getpersistentitemschangedsink">GetPersistentItemsChangedSink</a>
</td>
<td align="left" width="63%">
Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper">GetQueryHelper</a>
</td>
<td align="left" width="63%">
Gets the <a href="/windows/desktop/api/searchapi/nn-searchapi-isearchqueryhelper">ISearchQueryHelper</a> interface for the current catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-geturlindexingstate">GetURLIndexingState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-numberofitems">NumberOfItems</a>
</td>
<td align="left" width="63%">
Gets the number of items in the catalog.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-numberofitemstoindex">NumberOfItemsToIndex</a>
</td>
<td align="left" width="63%">
Gets the number of items to be indexed within the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-put_connecttimeout">put_ConnectTimeout</a>
</td>
<td align="left" width="63%">
Sets the connection time-out value in the <a href="/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> structure, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-put_datatimeout">put_DataTimeout</a>
</td>
<td align="left" width="63%">
Sets the time-out value for data transactions between the indexer and the search filter host. This information is stored in the <a href="/windows/desktop/api/searchapi/ns-searchapi-timeout_info">TIMEOUT_INFO</a> structure and is measured in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-put_diacriticsensitivity">put_DiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-registerviewfornotification">RegisterViewForNotification</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-reindex">Reindex</a>
</td>
<td align="left" width="63%">
Re-indexes all URLs in the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-reindexmatchingurls">ReindexMatchingURLs</a>
</td>
<td align="left" width="63%">
Reindexes all items that match the provided pattern. This method was not implemented prior to Windows 7.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-reindexsearchroot">ReindexSearchRoot</a>
</td>
<td align="left" width="63%">
Re-indexes all URLs from a specified root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the underlying catalog by rebuilding the databases and performing a full indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-setextensionclusion">SetExtensionClusion</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-setparameter">SetParameter</a>
</td>
<td align="left" width="63%">
Sets a name/value parameter for the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-unregisterviewfornotification">UnregisterViewForNotification</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-urlbeingindexed">URLBeingIndexed</a>
</td>
<td align="left" width="63%">
Gets the URL that is currently being indexed. If no indexing is currently in process, <i>pszUrl</i> is set to <b>NULL</b>.
        

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/search/-search-indexing-process-overview">The Indexing Process</a>