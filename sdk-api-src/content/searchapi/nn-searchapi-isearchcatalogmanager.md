---
UID: NN:searchapi.ISearchCatalogManager
title: ISearchCatalogManager (searchapi.h)
author: windows-sdk-content
description: Provides methods to manage a search catalog for purposes such as re-indexing or setting timeouts.
old-location: search\_search_ISearchCatalogManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\isearchcatalogmanager.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], ISearchCatalogManager interface [search],described, _search_ISearchCatalogManager, search._search_ISearchCatalogManager, searchapi/ISearchCatalogManager
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchCatalogManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchCatalogManager interface


## -description


Provides methods to manage a search catalog for purposes such as re-indexing or setting timeouts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCatalogManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchCatalogManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb231489(v=VS.85).aspx">EnumerateExcludedExtensions</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231497(v=VS.85).aspx">get_ConnectTimeout</a>
</td>
<td align="left" width="63%">
Gets the connection time-out value for connecting to a store for indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231498(v=VS.85).aspx">get_DataTimeout</a>
</td>
<td align="left" width="63%">
Gets the data time-out value, in seconds, for data transactions between the indexer and the search  filter host. This value is contained in a <a href="https://msdn.microsoft.com/en-us/library/Aa965374(v=VS.85).aspx">TIMEOUT_INFO</a> structure. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231499(v=VS.85).aspx">get_DiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231500(v=VS.85).aspx">get_Name</a>
</td>
<td align="left" width="63%">
Gets the name of the current catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231490(v=VS.85).aspx">GetCatalogStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231491(v=VS.85).aspx">GetCrawlScopeManager</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/en-us/library/Bb266492(v=VS.85).aspx">ISearchCrawlScopeManager</a> interface for this search catalog.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231492(v=VS.85).aspx">GetItemsChangedSink</a>
</td>
<td align="left" width="63%">
Gets the change notification sink interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231493(v=VS.85).aspx">GetParameter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231494(v=VS.85).aspx">GetPersistentItemsChangedSink</a>
</td>
<td align="left" width="63%">
Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231495(v=VS.85).aspx">GetQueryHelper</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/en-us/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a> interface for the current catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231496(v=VS.85).aspx">GetURLIndexingState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266415(v=VS.85).aspx">NumberOfItems</a>
</td>
<td align="left" width="63%">
Gets the number of items in the catalog.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266416(v=VS.85).aspx">NumberOfItemsToIndex</a>
</td>
<td align="left" width="63%">
Gets the number of items to be indexed within the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266417(v=VS.85).aspx">put_ConnectTimeout</a>
</td>
<td align="left" width="63%">
Sets the connection time-out value in the <a href="https://msdn.microsoft.com/en-us/library/Aa965374(v=VS.85).aspx">TIMEOUT_INFO</a> structure, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266418(v=VS.85).aspx">put_DataTimeout</a>
</td>
<td align="left" width="63%">
Sets the time-out value for data transactions between the indexer and the search filter host. This information is stored in the <a href="https://msdn.microsoft.com/en-us/library/Aa965374(v=VS.85).aspx">TIMEOUT_INFO</a> structure and is measured in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266419(v=VS.85).aspx">put_DiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266420(v=VS.85).aspx">RegisterViewForNotification</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266421(v=VS.85).aspx">Reindex</a>
</td>
<td align="left" width="63%">
Re-indexes all URLs in the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266422(v=VS.85).aspx">ReindexMatchingURLs</a>
</td>
<td align="left" width="63%">
Reindexes all items that match the provided pattern. This method was not implemented prior to Windows 7.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266423(v=VS.85).aspx">ReindexSearchRoot</a>
</td>
<td align="left" width="63%">
Re-indexes all URLs from a specified root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266424(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets the underlying catalog by rebuilding the databases and performing a full indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266425(v=VS.85).aspx">SetExtensionClusion</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266426(v=VS.85).aspx">SetParameter</a>
</td>
<td align="left" width="63%">
Sets a name/value parameter for the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266427(v=VS.85).aspx">UnregisterViewForNotification</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266428(v=VS.85).aspx">URLBeingIndexed</a>
</td>
<td align="left" width="63%">
Gets the URL that is currently being indexed. If no indexing is currently in process, <i>pszUrl</i> is set to <b>NULL</b>.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Cc678933(v=VS.85).aspx">The Indexing Process</a>
 

 

