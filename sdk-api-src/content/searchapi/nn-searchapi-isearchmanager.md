---
UID: NN:searchapi.ISearchManager
title: ISearchManager (searchapi.h)
author: windows-sdk-content
description: Provides methods for controlling the Search service. This interface manages settings and objects that affect the search engine across catalogs.
old-location: search\_search_ISearchManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\isearchmanager.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchManager, ISearchManager interface [search], ISearchManager interface [search],described, _search_ISearchManager, search._search_ISearchManager, searchapi/ISearchManager
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
req.idl: 
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
 - ISearchManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchManager interface


## -description


Provides methods for controlling the Search service. This interface manages settings and objects that affect the search engine across catalogs.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231479(v=VS.85).aspx">get_BypassList</a>
</td>
<td align="left" width="63%">
Gets a proxy bypass list from the indexer. This list is used to determine which items or URLs are local and do not need to go through the proxy server. This list is set by calling <a href="https://msdn.microsoft.com/en-us/library/Bb231488(v=VS.85).aspx">ISearchManager::SetProxy</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231480(v=VS.85).aspx">get_LocalBypass</a>
</td>
<td align="left" width="63%">
Retrieves a value that determines whether the proxy server should be bypassed to find the item or URL.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231481(v=VS.85).aspx">get_PortNumber</a>
</td>
<td align="left" width="63%">
Retrieves the port number used to communicate with the proxy server. This port number is stored in the indexer and is set by the <a href="https://msdn.microsoft.com/en-us/library/Bb231488(v=VS.85).aspx">ISearchManager::SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231482(v=VS.85).aspx">get_ProxyName</a>
</td>
<td align="left" width="63%">
Retrieves the proxy name to be used by the protocol handler.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231483(v=VS.85).aspx">get_UseProxy</a>
</td>
<td align="left" width="63%">
Retrieves the proxy server to be used.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231484(v=VS.85).aspx">get_UserAgent</a>
</td>
<td align="left" width="63%">
Retrieves the user agent string.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231475(v=VS.85).aspx">GetCatalog</a>
</td>
<td align="left" width="63%">
Retrieves a catalog by name and creates a new <a href="https://msdn.microsoft.com/en-us/library/Bb266414(v=VS.85).aspx">ISearchCatalogManager</a> object for that catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231476(v=VS.85).aspx">GetIndexerVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version of the current indexer in two chunks: the major version signifier and the minor version signifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231477(v=VS.85).aspx">GetIndexerVersionStr</a>
</td>
<td align="left" width="63%">
Retrieves the version of the current indexer as a single string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231478(v=VS.85).aspx">GetParameter</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231486(v=VS.85).aspx">put_UserAgent</a>
</td>
<td align="left" width="63%">
Sets the user agent string that a user agent passes to website and services to identify itself. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231487(v=VS.85).aspx">SetParameter</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231488(v=VS.85).aspx">SetProxy</a>
</td>
<td align="left" width="63%">
Stores information in the indexer that determines how the indexer will work and communicate with a proxy server.

</td>
</tr>
</table> 


## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



