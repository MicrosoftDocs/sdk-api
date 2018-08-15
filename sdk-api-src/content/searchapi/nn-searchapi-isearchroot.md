---
UID: NN:searchapi.ISearchRoot
title: ISearchRoot
author: windows-sdk-content
description: Provides methods for manipulating a search root. Changes to property members are applied to any URL that falls under the search root. A URL falls under a search root if it matches the search root URL or is a hierarchical child of that URL.
old-location: search\_search_ISearchRoot.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\isearchroot.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchRoot, ISearchRoot interface [search], ISearchRoot interface [search],described, _search_ISearchRoot, search._search_ISearchRoot, searchapi/ISearchRoot
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: searchapi.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchRoot interface


## -description


Provides methods for manipulating a search root. Changes to property members are applied to any URL that falls under the search root. A URL falls under a search root if it matches the search root URL or is a hierarchical child of that URL.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchRoot</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchRoot</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchRoot</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266458(v=VS.85).aspx">get_AuthenticationType</a>
</td>
<td align="left" width="63%">
Retrieves the type of authentication needed to access the URLs under this this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266459(v=VS.85).aspx">get_EnumerationDepth</a>
</td>
<td align="left" width="63%">
Gets the enumeration depth for this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266460(v=VS.85).aspx">get_FollowDirectories</a>
</td>
<td align="left" width="63%">
Gets a <b>BOOL</b> value that indicates whether the search engine follows subdirectories and hierarchical scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266461(v=VS.85).aspx">get_HostDepth</a>
</td>
<td align="left" width="63%">
Gets a value that indicates how far into a host tree to crawl when indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266462(v=VS.85).aspx">get_IsHierarchical</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the search is rooted on a hierarchical tree structure.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266463(v=VS.85).aspx">get_Password</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266464(v=VS.85).aspx">get_ProvidesNotifications</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266465(v=VS.85).aspx">get_RootURL</a>
</td>
<td align="left" width="63%">
Gets the URL of the starting point for this search root.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266466(v=VS.85).aspx">get_Schedule</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266467(v=VS.85).aspx">get_UseNotificationsOnly</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether this search root should be indexed only by notification and not crawled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266468(v=VS.85).aspx">get_User</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266470(v=VS.85).aspx">put_AuthenticationType</a>
</td>
<td align="left" width="63%">
Sets the type of authentication required to access the URLs under this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266471(v=VS.85).aspx">put_EnumerationDepth</a>
</td>
<td align="left" width="63%">
Sets the enumeration depth for this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266472(v=VS.85).aspx">put_FollowDirectories</a>
</td>
<td align="left" width="63%">
Sets a <b>BOOL</b> value that indicates whether the search engine should follow subdirectories and hierarchical scopes for this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266473(v=VS.85).aspx">put_HostDepth</a>
</td>
<td align="left" width="63%">
Sets a value that indicates how far into a host tree to crawl when indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266474(v=VS.85).aspx">put_IsHierarchical</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether the search is rooted on a hierarchical tree structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266475(v=VS.85).aspx">put_Password</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266476(v=VS.85).aspx">put_ProvidesNotifications</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266477(v=VS.85).aspx">put_RootURL</a>
</td>
<td align="left" width="63%">
Sets the URL of the current search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266478(v=VS.85).aspx">put_Schedule</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266479(v=VS.85).aspx">put_User</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266480(v=VS.85).aspx">set_UseNotificationsOnly</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether this search root should be indexed only by notification and not crawled.

</td>
</tr>
</table> 


## -remarks



The CrawlScopeCommandLine code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to define command line 
options for Crawl Scope Manager (CSM) indexing operations.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb266541(v=VS.85).aspx">Using the Crawl Scope Manager</a>
 

 

