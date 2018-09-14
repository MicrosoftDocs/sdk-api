---
UID: NF:searchapi.ISearchQueryHelper.GenerateSQLFromUserQuery
title: ISearchQueryHelper::GenerateSQLFromUserQuery
author: windows-sdk-content
description: Generates a Structured Query Language (SQL) query based on a client-supplied query string expressed in either Advanced Query Syntax (AQS) or Natural Query Syntax (NQS).
old-location: search\_search_ISearchQueryHelper_GenerateSQLFromUserQuery.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\generatesqlfromuserquery.htm
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GenerateSQLFromUserQuery, GenerateSQLFromUserQuery method [search], GenerateSQLFromUserQuery method [search],ISearchQueryHelper interface, ISearchQueryHelper interface [search],GenerateSQLFromUserQuery method, ISearchQueryHelper.GenerateSQLFromUserQuery, ISearchQueryHelper::GenerateSQLFromUserQuery, _search_ISearchQueryHelper_GenerateSQLFromUserQuery, search._search_ISearchQueryHelper_GenerateSQLFromUserQuery, searchapi/ISearchQueryHelper::GenerateSQLFromUserQuery
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISearchQueryHelper.GenerateSQLFromUserQuery
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ISearchQueryHelper::GenerateSQLFromUserQuery


## -description


Generates a Structured Query Language (SQL) query based on a client-supplied query string expressed in either Advanced Query Syntax (AQS) or Natural Query Syntax (NQS).


## -parameters




### -param pszQuery [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated Unicode string containing a query in AQS or NQS.


### -param ppszSQL [out, retval]

Type: <b>LPWSTR*</b>

Receives the address of a pointer to a SQL query string based on the query in the <i>pszQuery</i> parameter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method generates SQL in the following form:

<pre class="syntax" xml:space="preserve"><code>SELECT &lt;QuerySelectColumns&gt; FROM &lt;CatalogName that created query helper&gt;
    WHERE &lt;Result of interpreting the User query passed into this function according to QuerySyntax&gt;
          [ AND|OR &lt;QueryWhereRestrictions&gt;]</code></pre>
The SQL generation uses the settings specified in <a href="https://msdn.microsoft.com/en-us/library/Bb231321(v=VS.85).aspx">ISearchQueryHelper::put_QueryTermExpansion</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb231315(v=VS.85).aspx">ISearchQueryHelper::put_QueryContentProperties</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb231314(v=VS.85).aspx">ISearchQueryHelper::put_QueryContentLocale</a>.

<b>ISearchQueryHelper::GenerateSQLFromUserQuery</b> uses regional locale settings. However, <a href="https://msdn.microsoft.com/en-us/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a> does not use the regional locale settings. As a result, there are inconsistencies in the SQL returned from <b>ISearchQueryHelper::GenerateSQLFromUserQuery</b> and <b>ISearchQueryHelper</b> for region specific settings such as  date formats. For example, if you set the locale for date/time to something other than the system locale, such as en-CA if the system locale is en-US, and enter <code>Toybox -m -i "date:3/7/2008" -Y -s</code>, the SQL returned will differ. The SQL from <b>ISearchQueryHelper::GenerateSQLFromUserQuery</b> will have parsed 3/7/2008 according to en-CA (seeking items dated 3rd of July, 2008) while the SQL from <b>ISearchQueryHelper</b> will have parsed 3/7/2008 according to en-US (seeking items dated 7th of March, 2008).

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/en-us/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb231313(v=VS.85).aspx">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231310(v=VS.85).aspx">ISearchQueryHelper::get_QuerySyntax</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb266517(v=VS.85).aspx">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231256(v=VS.85).aspx">Querying the Index with Windows Search SQL Syntax</a>
 

 

