---
UID: NN:searchapi.ISearchRoot
title: ISearchRoot
author: windows-sdk-content
description: Provides methods for manipulating a search root. Changes to property members are applied to any URL that falls under the search root. A URL falls under a search root if it matches the search root URL or is a hierarchical child of that URL.
old-location: search\_search_ISearchRoot.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\crawlscope\isearchroot\isearchroot.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ISearchRoot, ISearchRoot interface [search], ISearchRoot interface [search],described, _search_ISearchRoot, search._search_ISearchRoot, searchapi/ISearchRoot
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
-	ISearchRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
<a href="https://msdn.microsoft.com/6f9e12b0-af88-4338-a323-ba6b6b4a5cef">get_AuthenticationType</a>
</td>
<td align="left" width="63%">
Retrieves the type of authentication needed to access the URLs under this this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f935d5ce-981c-430c-88eb-09dd7a364751">get_EnumerationDepth</a>
</td>
<td align="left" width="63%">
Gets the enumeration depth for this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bade7d3a-5286-4647-8e55-ff2d70033a4d">get_FollowDirectories</a>
</td>
<td align="left" width="63%">
Gets a <b>BOOL</b> value that indicates whether the search engine follows subdirectories and hierarchical scopes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c76073e-ae7b-4b25-b5c1-3f89280adf59">get_HostDepth</a>
</td>
<td align="left" width="63%">
Gets a value that indicates how far into a host tree to crawl when indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6318234-e9e5-4341-873d-bd4b13977ecc">get_IsHierarchical</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the search is rooted on a hierarchical tree structure.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbe90835-0619-45f1-a7d4-f11b4bd644cc">get_Password</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/050c20f9-759b-4bb2-8dce-801006440a40">get_ProvidesNotifications</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efc7637b-f679-45d2-b189-12db29374181">get_RootURL</a>
</td>
<td align="left" width="63%">
Gets the URL of the starting point for this search root.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8897f437-5b66-46df-820f-e9d014e6fb02">get_Schedule</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f2e1dd4-d722-4690-92c1-8305a199b312">get_UseNotificationsOnly</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether this search root should be indexed only by notification and not crawled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25679e72-b65c-4219-90e3-d4b9a35c3597">get_User</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c443c8a-6ad9-46c5-987b-9e8e705f705f">put_AuthenticationType</a>
</td>
<td align="left" width="63%">
Sets the type of authentication required to access the URLs under this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b589ec6-224a-48f1-98f0-e3a7cf7651be">put_EnumerationDepth</a>
</td>
<td align="left" width="63%">
Sets the enumeration depth for this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46363caa-5571-4d22-873d-6dabbc1753df">put_FollowDirectories</a>
</td>
<td align="left" width="63%">
Sets a <b>BOOL</b> value that indicates whether the search engine should follow subdirectories and hierarchical scopes for this search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7efb7a75-1864-4fb7-81bc-fbff744d0f1c">put_HostDepth</a>
</td>
<td align="left" width="63%">
Sets a value that indicates how far into a host tree to crawl when indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c31dffa4-e6d9-4250-af50-5b9c49e2b15c">put_IsHierarchical</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether the search is rooted on a hierarchical tree structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68a8e162-4889-4404-ba1e-98fb780afab4">put_Password</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45a87b46-7c87-451d-a3f7-b9ead74f24b6">put_ProvidesNotifications</a>
</td>
<td align="left" width="63%">
Sets a value that indicates whether the search engine is notified (by protocol handlers or other applications) about changes to the URLs under the search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/704b9866-dafe-4dcf-bc3e-af3d47695f99">put_RootURL</a>
</td>
<td align="left" width="63%">
Sets the URL of the current search root.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a226481-a676-484d-99c6-e9c9bec8d461">put_Schedule</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/706eb3a6-271f-4154-b547-10cb2bdf5c13">put_User</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf1869f1-fd60-4b81-957e-cae6f7dd5865">set_UseNotificationsOnly</a>
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




<a href="https://msdn.microsoft.com/7d65d00a-7294-4718-b593-89394b2e416f">Using the Crawl Scope Manager</a>
 

 

