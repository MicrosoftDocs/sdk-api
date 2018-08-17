---
UID: NN:searchapi.ISearchQueryHelper
title: ISearchQueryHelper
author: windows-sdk-content
description: Provides methods for building a query from user input, converting a query to Windows Search SQL, and obtaining a connection string to initialize a connection to the Window Search index.
old-location: search\_search_ISearchQueryHelper.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\isearchqueryhelper.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchQueryHelper, ISearchQueryHelper interface [search], ISearchQueryHelper interface [search],described, _search_ISearchQueryHelper, search._search_ISearchQueryHelper, searchapi/ISearchQueryHelper
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
req.idl: Searchquery.idl
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
 - ISearchQueryHelper
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchQueryHelper interface


## -description


Provides methods for building a query from user input, converting a query to <a href="https://msdn.microsoft.com/7d992fa2-4606-46ca-904c-b45056a9bbc2">Windows Search SQL</a>, and obtaining a connection string to initialize a connection to the Window Search index. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchQueryHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISearchQueryHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISearchQueryHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/846c0c05-c227-487c-8512-7644b80db8d8">GenerateSQLFromUserQuery</a>
</td>
<td align="left" width="63%">
Generates a SQL query based on a client-supplied query string expressed in either Advanced Query Syntax (AQS) or Natural Query Syntax (NQS).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d4d6a75-3be4-4b18-b76a-1a9ca76e2ffb">get_ConnectionString</a>
</td>
<td align="left" width="63%">
Returns the OLE DB connection string for the Window Search index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71ce4dad-7867-4844-abec-f647eef0a7c1">get_QueryContentLocale</a>
</td>
<td align="left" width="63%">
Gets the LCID for the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b1df4af-6210-4bd8-949c-d0cc5f1afe5d">get_QueryContentProperties</a>
</td>
<td align="left" width="63%">
Gets the list of properties included in the query when search terms do not explicitly specify a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4344d24-cc16-4da8-a70d-1f74e33d551e">get_QueryKeywordLocale</a>
</td>
<td align="left" width="63%">
Gets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0922d84-e370-484b-b412-065aabbf3db1">get_QueryMaxResults</a>
</td>
<td align="left" width="63%">
Gets the maximum number of results to be returned by the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1496e880-9dd0-40a5-97e7-2a9367bf9127">get_QuerySelectColumns</a>
</td>
<td align="left" width="63%">
Gets the columns (or properties) requested in the SELECT statement of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7539d055-bff9-436c-abd1-11e2ff5ed858">get_QuerySorting</a>
</td>
<td align="left" width="63%">
Gets the sort order for the query result set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72802fbc-6684-40e3-9df5-a81e2c4bc1c2">get_QuerySyntax</a>
</td>
<td align="left" width="63%">
Gets the syntax of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3af83c74-e2af-40f1-afdd-fec286b42be2">get_QueryTermExpansion</a>
</td>
<td align="left" width="63%">
Gets the value that specifies how query terms are to be expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec0082aa-381f-4efe-8626-aa586ae030f3">get_QueryWhereRestrictions</a>
</td>
<td align="left" width="63%">
Gets the restrictions appended to a query in WHERE clauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e444ad37-6bbd-4408-882b-815193a098bf">put_QueryContentLocale</a>
</td>
<td align="left" width="63%">
Sets the LCID of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75d4882c-305a-4035-9c8c-e72de3c6812f">put_QueryContentProperties</a>
</td>
<td align="left" width="63%">
Sets the properties to include in the query if search terms do not explicitly specify properties. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6530db1a-260a-4925-be4a-549e42464983">put_QueryKeywordLocale</a>
</td>
<td align="left" width="63%">
Sets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c260972-d7b6-4b1e-8dcd-4c8e22bb3017">put_QueryMaxResults</a>
</td>
<td align="left" width="63%">
Sets the maximum number of results to be returned by a query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99c965a3-6c62-4d86-a007-fb75b5a2bbef">put_QuerySelectColumns</a>
</td>
<td align="left" width="63%">
Sets the columns (or properties) requested in the select statement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ff2978a-3487-432e-84e8-4234a251d8d7">put_QuerySorting</a>
</td>
<td align="left" width="63%">
Sets the sort order for the query result set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4df77a77-10fd-411c-bd35-450ffdbc1da8">put_QuerySyntax</a>
</td>
<td align="left" width="63%">
Sets the syntax of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edcc8a86-b677-4f84-aa6f-90ada895dbcc">put_QueryTermExpansion</a>
</td>
<td align="left" width="63%">
Sets a value that specifies how query terms are to be expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d7f218f-1abc-4f9a-94f7-bb9311097193">put_QueryWhereRestrictions</a>
</td>
<td align="left" width="63%">
Sets the restrictions appended to a query in WHERE clauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5e2caa2-73e8-43f1-a83b-018f8aefea7a">WriteProperties</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling <a href="https://msdn.microsoft.com/82894b06-57d4-404b-9527-f62efb346e77">ISearchCatalogManager::GetQueryHelper</a>. Implement this interface as a helper class to <a href="https://msdn.microsoft.com/098e0574-53af-4b52-99e7-659f98b914ae">ISearchCatalogManager</a>.

This interface facilitates the generation of SQL queries using Advanced Query Syntax (AQS) or Natural Query Syntax (NQS). Clients can submit the SQL query to the Window Search engine by using OLE DB or Microsoft ActiveX Data Objects (ADO).


<a href="https://msdn.microsoft.com/846c0c05-c227-487c-8512-7644b80db8d8">ISearchQueryHelper::GenerateSQLFromUserQuery</a> uses regional locale settings. However, <b>ISearchQueryHelper</b> does not use the regional locale settings. As a result, there are inconsistencies in the SQL returned from <b>ISearchQueryHelper::GenerateSQLFromUserQuery</b> and <b>ISearchQueryHelper</b> for region specific settings such as date formats, for example.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <b>ISearchQueryHelper</b>.




## -see-also




<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

