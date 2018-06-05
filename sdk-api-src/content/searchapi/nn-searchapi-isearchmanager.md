---
UID: NN:searchapi.ISearchManager
title: ISearchManager
author: windows-sdk-content
description: Provides methods for controlling the Search service. This interface manages settings and objects that affect the search engine across catalogs.
old-location: search\_search_ISearchManager.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\indexmanagement\isearchmanager\isearchmanager.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchManager, ISearchManager interface [search], ISearchManager interface [search],described, _search_ISearchManager, search._search_ISearchManager, searchapi/ISearchManager
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Searchapi.h
api_name:
-	ISearchManager
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/63ee4f65-cb0f-432c-b3a1-379e3dc853be">get_BypassList</a>
</td>
<td align="left" width="63%">
Gets a proxy bypass list from the indexer. This list is used to determine which items or URLs are local and do not need to go through the proxy server. This list is set by calling <a href="https://msdn.microsoft.com/93fc8bb8-9cec-4c3a-8a7f-a988e931f803">ISearchManager::SetProxy</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/438d921e-9149-43c4-9ed9-422914f3a0d4">get_LocalBypass</a>
</td>
<td align="left" width="63%">

            Retrieves a value that determines whether the proxy server should be bypassed to find the item or URL.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/918e2cbf-88c6-4c15-b186-8d7d6f5676c1">get_PortNumber</a>
</td>
<td align="left" width="63%">

            Retrieves the port number used to communicate with the proxy server. This port number is stored in the indexer and is set by the <a href="https://msdn.microsoft.com/93fc8bb8-9cec-4c3a-8a7f-a988e931f803">ISearchManager::SetProxy</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bfd6942-b1e8-4702-80bf-8bcf59474a0a">get_ProxyName</a>
</td>
<td align="left" width="63%">

            Retrieves the proxy name to be used by the protocol handler.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac96c52a-51ed-426d-8958-70b0c898bc3d">get_UseProxy</a>
</td>
<td align="left" width="63%">

            Retrieves the proxy server to be used.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a68cd25b-3c96-4e4f-8a56-03977771e549">get_UserAgent</a>
</td>
<td align="left" width="63%">

            Retrieves the user agent string.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/921ae63a-c9fd-433c-8085-5a8d56b4b157">GetCatalog</a>
</td>
<td align="left" width="63%">

            Retrieves a catalog by name and creates a new <a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a> object for that catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d68f03e-08ae-4eaa-9a30-844b42640edd">GetIndexerVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version of the current indexer in two chunks: the major version signifier and the minor version signifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09786600-952c-4fbb-a75d-4773e3f2864f">GetIndexerVersionStr</a>
</td>
<td align="left" width="63%">
Retrieves the version of the current indexer as a single string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e057e1e-4cbd-43d2-9570-25b89f61b111">GetParameter</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe44cde7-c156-4255-a5b3-3d5001553484">put_UserAgent</a>
</td>
<td align="left" width="63%">

            Sets the user agent string that a user agent passes to website and services to identify itself. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/168cafe8-a887-4037-a5f9-8818b7d79566">SetParameter</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93fc8bb8-9cec-4c3a-8a7f-a988e931f803">SetProxy</a>
</td>
<td align="left" width="63%">
Stores information in the indexer that determines how the indexer will work and communicate with a proxy server.

</td>
</tr>
</table> 


## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



