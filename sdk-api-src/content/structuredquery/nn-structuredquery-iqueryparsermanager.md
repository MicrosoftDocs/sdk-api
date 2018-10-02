---
UID: NN:structuredquery.IQueryParserManager
title: IQueryParserManager
author: windows-sdk-content
description: Provides methods to create, initialize, and change options for an IQueryParser object.
old-location: search\_search_IQueryParserManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\iqueryparsermanager.htm
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IQueryParserManager, IQueryParserManager interface [search], IQueryParserManager interface [search],described, _search_IQueryParserManager, search._search_IQueryParserManager, structuredquery/IQueryParserManager
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquery.idl
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
 - Structuredquery.h
api_name:
 - IQueryParserManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IQueryParserManager interface


## -description


Provides methods to create, initialize, and change options for an <a href="https://msdn.microsoft.com/en-us/library/Bb231353(v=VS.85).aspx">IQueryParser</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryParserManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQueryParserManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryParserManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231347(v=VS.85).aspx">CreateLoadedParser</a>
</td>
<td align="left" width="63%">
Creates a new instance of a <a href="https://msdn.microsoft.com/en-us/library/Bb231353(v=VS.85).aspx">IQueryParser</a> interface implementation. This instance of the query parser is loaded with the schema for the specified catalog and is localized to a specified language. All other settings are initialized to default settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231348(v=VS.85).aspx">InitializeOptions</a>
</td>
<td align="left" width="63%">
Sets the flags for Natural Query Syntax (NQS) and automatic wildcard characters for the specified query parser. If the query parser was created for the <code>SystemIndex</code> catalog, this method also sets up standard condition generators to be used later by the query parser object for recognizing named entities.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231350(v=VS.85).aspx">SetOption</a>
</td>
<td align="left" width="63%">
Changes a single option in this <b>IQueryParserManager</b> object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965711(v=VS.85).aspx">Advanced Query Syntax</a>
 

 

