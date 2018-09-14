---
UID: NN:searchapi.ISearchCatalogManager
title: ISearchCatalogManager
author: windows-sdk-content
description: Provides methods to manage a search catalog for purposes such as re-indexing or setting timeouts.
old-location: search\_search_ISearchCatalogManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchcatalogmanager\isearchcatalogmanager.htm
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ISearchCatalogManager, ISearchCatalogManager interface [search], ISearchCatalogManager interface [search],described, _search_ISearchCatalogManager, search._search_ISearchCatalogManager, searchapi/ISearchCatalogManager
ms.prod: windows
ms.technology: windows-sdk
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
<a href="https://msdn.microsoft.com/1263b88f-6e58-4107-b9a5-dca55551670f">EnumerateExcludedExtensions</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86bcb5c9-813f-462a-a859-dd47127dff10">get_ConnectTimeout</a>
</td>
<td align="left" width="63%">
Gets the connection time-out value for connecting to a store for indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81f02e23-3f7c-4989-a39e-d5c6883e9493">get_DataTimeout</a>
</td>
<td align="left" width="63%">
Gets the data time-out value, in seconds, for data transactions between the indexer and the search  filter host. This value is contained in a <a href="https://msdn.microsoft.com/f6032470-abfd-4808-921c-7fa687ed640f">TIMEOUT_INFO</a> structure. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed11b5ba-c939-4efc-87c1-358796397f09">get_DiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/440e3bdf-7cfd-4e6f-8274-159300d27501">get_Name</a>
</td>
<td align="left" width="63%">
Gets the name of the current catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22cd866e-8af7-428a-8036-43f5ac9ad099">GetCatalogStatus</a>
</td>
<td align="left" width="63%">
Gets the status of the catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/420204ca-10c4-4f37-933c-eb3f24d2bd76">GetCrawlScopeManager</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/8b731941-f1f6-402e-8cee-3c493e3c369d">ISearchCrawlScopeManager</a> interface for this search catalog.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1637859-369a-4d67-984d-09babbf0be98">GetItemsChangedSink</a>
</td>
<td align="left" width="63%">
Gets the change notification sink interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a877a2b0-49aa-4df4-8e4e-16736a6b3804">GetParameter</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e673c9c-8e50-4b4e-8bdf-4b1e785e0fc5">GetPersistentItemsChangedSink</a>
</td>
<td align="left" width="63%">
Gets the change notification event sink interface for a client. This method is used by client applications and protocol handlers to notify the indexer of changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82894b06-57d4-404b-9527-f62efb346e77">GetQueryHelper</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a> interface for the current catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0f4a0b9-6688-4a36-8867-e66498a113ab">GetURLIndexingState</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/721de587-ab21-467b-a97b-e0d80ba9ccaa">NumberOfItems</a>
</td>
<td align="left" width="63%">
Gets the number of items in the catalog.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc82c814-865a-47fe-8541-d79eeee0b8df">NumberOfItemsToIndex</a>
</td>
<td align="left" width="63%">
Gets the number of items to be indexed within the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98805e77-4d9a-4857-bd58-9559c729b432">put_ConnectTimeout</a>
</td>
<td align="left" width="63%">
Sets the connection time-out value in the <a href="https://msdn.microsoft.com/f6032470-abfd-4808-921c-7fa687ed640f">TIMEOUT_INFO</a> structure, in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cb970e3-c939-47e7-a713-f1b6f084460f">put_DataTimeout</a>
</td>
<td align="left" width="63%">
Sets the time-out value for data transactions between the indexer and the search filter host. This information is stored in the <a href="https://msdn.microsoft.com/f6032470-abfd-4808-921c-7fa687ed640f">TIMEOUT_INFO</a> structure and is measured in seconds.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c680ec4c-c850-4486-b317-80c82584ee95">put_DiacriticSensitivity</a>
</td>
<td align="left" width="63%">
Sets a value that determines whether the catalog is sensitive to diacritics. A diacritic is a mark added to a letter to indicate a special phonetic value or pronunciation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/608a35f7-3c5c-4e1d-b7fc-7c1ab5327af1">RegisterViewForNotification</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d7fa3d1-2cda-4ec5-ae20-fe5f7b8c0c82">Reindex</a>
</td>
<td align="left" width="63%">
Re-indexes all URLs in the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b16496e-ae03-4ea9-ac9e-307b087b864e">ReindexMatchingURLs</a>
</td>
<td align="left" width="63%">
Reindexes all items that match the provided pattern. This method was not implemented prior to Windows 7.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed2bc32a-e5a0-471f-ba49-fcc70d991690">ReindexSearchRoot</a>
</td>
<td align="left" width="63%">
Re-indexes all URLs from a specified root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95af7d31-b88e-47d5-bf8c-b5428ab860cc">Reset</a>
</td>
<td align="left" width="63%">
Resets the underlying catalog by rebuilding the databases and performing a full indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eba632e4-cbba-457a-ab89-cb4316507c39">SetExtensionClusion</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cefa86a-b6cb-4f0b-a2f9-1647f2696706">SetParameter</a>
</td>
<td align="left" width="63%">
Sets a name/value parameter for the catalog.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9d3c86c-e36e-4127-8b2f-1bdfe9057f41">UnregisterViewForNotification</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ecd6168-92da-46b5-9c61-86ed99950413">URLBeingIndexed</a>
</td>
<td align="left" width="63%">
Gets the URL that is currently being indexed. If no indexing is currently in process, <i>pszUrl</i> is set to <b>NULL</b>.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

