---
UID: NN:searchapi.ISearchQueryHelper
title: ISearchQueryHelper (searchapi.h)
author: windows-sdk-content
description: Provides methods for building a query from user input, converting a query to Windows Search SQL, and obtaining a connection string to initialize a connection to the Window Search index.
old-location: search\_search_ISearchQueryHelper.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\isearchqueryhelper.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISearchQueryHelper, ISearchQueryHelper interface [search], ISearchQueryHelper interface [search],described, _search_ISearchQueryHelper, search._search_ISearchQueryHelper, searchapi/ISearchQueryHelper
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchQueryHelper interface


## -description


Provides methods for building a query from user input, converting a query to <a href="https://msdn.microsoft.com/en-us/library/Bb231255(v=VS.85).aspx">Windows Search SQL</a>, and obtaining a connection string to initialize a connection to the Window Search index. 


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
<a href="https://msdn.microsoft.com/en-us/library/Bb231302(v=VS.85).aspx">GenerateSQLFromUserQuery</a>
</td>
<td align="left" width="63%">
Generates a SQL query based on a client-supplied query string expressed in either Advanced Query Syntax (AQS) or Natural Query Syntax (NQS).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231303(v=VS.85).aspx">get_ConnectionString</a>
</td>
<td align="left" width="63%">
Returns the OLE DB connection string for the Window Search index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231304(v=VS.85).aspx">get_QueryContentLocale</a>
</td>
<td align="left" width="63%">
Gets the LCID for the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231305(v=VS.85).aspx">get_QueryContentProperties</a>
</td>
<td align="left" width="63%">
Gets the list of properties included in the query when search terms do not explicitly specify a property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231306(v=VS.85).aspx">get_QueryKeywordLocale</a>
</td>
<td align="left" width="63%">
Gets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231307(v=VS.85).aspx">get_QueryMaxResults</a>
</td>
<td align="left" width="63%">
Gets the maximum number of results to be returned by the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231308(v=VS.85).aspx">get_QuerySelectColumns</a>
</td>
<td align="left" width="63%">
Gets the columns (or properties) requested in the SELECT statement of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231309(v=VS.85).aspx">get_QuerySorting</a>
</td>
<td align="left" width="63%">
Gets the sort order for the query result set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231310(v=VS.85).aspx">get_QuerySyntax</a>
</td>
<td align="left" width="63%">
Gets the syntax of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231311(v=VS.85).aspx">get_QueryTermExpansion</a>
</td>
<td align="left" width="63%">
Gets the value that specifies how query terms are to be expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231312(v=VS.85).aspx">get_QueryWhereRestrictions</a>
</td>
<td align="left" width="63%">
Gets the restrictions appended to a query in WHERE clauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231314(v=VS.85).aspx">put_QueryContentLocale</a>
</td>
<td align="left" width="63%">
Sets the LCID of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231315(v=VS.85).aspx">put_QueryContentProperties</a>
</td>
<td align="left" width="63%">
Sets the properties to include in the query if search terms do not explicitly specify properties. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231316(v=VS.85).aspx">put_QueryKeywordLocale</a>
</td>
<td align="left" width="63%">
Sets the LCID for the locale to use when parsing Advanced Query Syntax (AQS) keywords.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231317(v=VS.85).aspx">put_QueryMaxResults</a>
</td>
<td align="left" width="63%">
Sets the maximum number of results to be returned by a query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231318(v=VS.85).aspx">put_QuerySelectColumns</a>
</td>
<td align="left" width="63%">
Sets the columns (or properties) requested in the select statement.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231319(v=VS.85).aspx">put_QuerySorting</a>
</td>
<td align="left" width="63%">
Sets the sort order for the query result set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231320(v=VS.85).aspx">put_QuerySyntax</a>
</td>
<td align="left" width="63%">
Sets the syntax of the query.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231321(v=VS.85).aspx">put_QueryTermExpansion</a>
</td>
<td align="left" width="63%">
Sets a value that specifies how query terms are to be expanded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231322(v=VS.85).aspx">put_QueryWhereRestrictions</a>
</td>
<td align="left" width="63%">
Sets the restrictions appended to a query in WHERE clauses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231323(v=VS.85).aspx">WriteProperties</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by calling <a href="https://msdn.microsoft.com/en-us/library/Bb231495(v=VS.85).aspx">ISearchCatalogManager::GetQueryHelper</a>. Implement this interface as a helper class to <a href="https://msdn.microsoft.com/en-us/library/Bb266414(v=VS.85).aspx">ISearchCatalogManager</a>.

This interface facilitates the generation of SQL queries using Advanced Query Syntax (AQS) or Natural Query Syntax (NQS). Clients can submit the SQL query to the Window Search engine by using OLE DB or Microsoft ActiveX Data Objects (ADO).


<a href="https://msdn.microsoft.com/en-us/library/Bb231302(v=VS.85).aspx">ISearchQueryHelper::GenerateSQLFromUserQuery</a> uses regional locale settings. However, <b>ISearchQueryHelper</b> does not use the regional locale settings. As a result, there are inconsistencies in the SQL returned from <b>ISearchQueryHelper::GenerateSQLFromUserQuery</b> and <b>ISearchQueryHelper</b> for region specific settings such as date formats, for example.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <b>ISearchQueryHelper</b>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb266517(v=VS.85).aspx">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231256(v=VS.85).aspx">Querying the Index with Windows Search SQL Syntax</a>
 

 

