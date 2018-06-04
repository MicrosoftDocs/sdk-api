---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISearchCatalogManager2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a> interface to manage a search catalog, for purposes such as re-indexing or setting timeouts. Applications can use this interface to attempt to reindex items that failed to be indexed previously, using the <a href="https://msdn.microsoft.com/ac8f8952-79a4-490e-bb62-6e2902e47b6e">PrioritizeMatchingURLs</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchCatalogManager2</b> interface inherits from <a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a>. <b>ISearchCatalogManager2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchCatalogManager2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac8f8952-79a4-490e-bb62-6e2902e47b6e">PrioritizeMatchingURLs</a>
</td>
<td align="left" width="63%">
Instructs the indexer to give a higher priority to indexing items that have URLs that match a specified pattern. These items will then have a higher priority than other indexing tasks.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a>



<a href="https://msdn.microsoft.com/cfba12eb-4123-4b57-8311-d4fc8f9f514e">The Indexing Process</a>
 

 

