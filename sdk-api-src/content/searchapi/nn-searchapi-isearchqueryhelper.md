---
UID: NN:searchapi.ISearchQueryHelper
title: ISearchQueryHelper (searchapi.h)
description: Provides methods for building a query from user input, converting a query to Windows Search SQL, and obtaining a connection string to initialize a connection to the Window Search index.
old-location: search\_search_ISearchQueryHelper.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\isearchqueryhelper.htm
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper, ISearchQueryHelper interface [search], ISearchQueryHelper interface [search],described, _search_ISearchQueryHelper, search._search_ISearchQueryHelper, searchapi/ISearchQueryHelper
f1_keywords:
- searchapi/ISearchQueryHelper
dev_langs:
- c++
req.header: searchapi.h
req.include-header: 
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
- ISearchQueryHelper
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ISearchQueryHelper interface


## -description


Provides methods for building a query from user input, converting a query to <a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-ovwofsearchquery">Windows Search SQL</a>, and obtaining a connection string to initialize a connection to the Window Search index. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISearchQueryHelper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISearchQueryHelper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery">GenerateSQLFromUserQuery</a>
</td>
<td align="left" width="63%">
Generates a SQL query based on a client-supplied query string expressed in either Advanced Query Syntax (AQS) or Natural Query Syntax (NQS).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring">get_ConnectionString</a>
</td>
<td align="left" width="63%">
Returns the OLE DB connection string for the Window Search index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale">get_QueryContentLocale</a>
</td>
<td align="left" width="63%">
Gets the LCID for the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties">get_QueryContentProperties</a>
</td>
<td align="left" width="63%">
Gets the list of properties included in the query when search terms do not explicitly specify a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale">get_QueryKeywordLocale</a>
</td>
<td align="left" width="63%">
Gets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults">get_QueryMaxResults</a>
</td>
<td align="left" width="63%">
Gets the maximum number of results to be returned by the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns">get_QuerySelectColumns</a>
</td>
<td align="left" width="63%">
Gets the columns (or properties) requested in the SELECT statement of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querysorting">get_QuerySorting</a>
</td>
<td align="left" width="63%">
Gets the sort order for the query result set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax">get_QuerySyntax</a>
</td>
<td align="left" width="63%">
Gets the syntax of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion">get_QueryTermExpansion</a>
</td>
<td align="left" width="63%">
Gets the value that specifies how query terms are to be expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions">get_QueryWhereRestrictions</a>
</td>
<td align="left" width="63%">
Gets the restrictions appended to a query in WHERE clauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale">put_QueryContentLocale</a>
</td>
<td align="left" width="63%">
Sets the LCID of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties">put_QueryContentProperties</a>
</td>
<td align="left" width="63%">
Sets the properties to include in the query if search terms do not explicitly specify properties. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale">put_QueryKeywordLocale</a>
</td>
<td align="left" width="63%">
Sets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults">put_QueryMaxResults</a>
</td>
<td align="left" width="63%">
Sets the maximum number of results to be returned by a query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns">put_QuerySelectColumns</a>
</td>
<td align="left" width="63%">
Sets the columns (or properties) requested in the select statement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querysorting">put_QuerySorting</a>
</td>
<td align="left" width="63%">
Sets the sort order for the query result set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax">put_QuerySyntax</a>
</td>
<td align="left" width="63%">
Sets the syntax of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion">put_QueryTermExpansion</a>
</td>
<td align="left" width="63%">
Sets a value that specifies how query terms are to be expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions">put_QueryWhereRestrictions</a>
</td>
<td align="left" width="63%">
Sets the restrictions appended to a query in WHERE clauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-writeproperties">WriteProperties</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper">ISearchCatalogManager::GetQueryHelper</a>. Implement this interface as a helper class to <a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a>.

This interface facilitates the generation of SQL queries using Advanced Query Syntax (AQS) or Natural Query Syntax (NQS). Clients can submit the SQL query to the Window Search engine by using OLE DB or Microsoft ActiveX Data Objects (ADO).


<a href="https://docs.microsoft.com/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery">ISearchQueryHelper::GenerateSQLFromUserQuery</a> uses regional locale settings. However, <b>ISearchQueryHelper</b> does not use the regional locale settings. As a result, there are inconsistencies in the SQL returned from <b>ISearchQueryHelper::GenerateSQLFromUserQuery</b> and <b>ISearchQueryHelper</b> for region specific settings such as date formats, for example.

The DSearch code sample, available on <a href="https://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="https://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <b>ISearchQueryHelper</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-qryidx-overview">Querying the Index Programmatically</a>



<a href="https://docs.microsoft.com/windows/desktop/search/-search-sql-windowssearch-entry">Querying the Index with Windows Search SQL Syntax</a>
 

 

