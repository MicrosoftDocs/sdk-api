---
UID: NN:structuredquery.IQueryParserManager
title: IQueryParserManager (structuredquery.h)
description: Provides methods to create, initialize, and change options for an IQueryParser object.
helpviewer_keywords: ["IQueryParserManager","IQueryParserManager interface [search]","IQueryParserManager interface [search]","described","_search_IQueryParserManager","search._search_IQueryParserManager","structuredquery/IQueryParserManager"]
old-location: search\_search_IQueryParserManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\iqueryparsermanager.htm
ms.date: 12/05/2018
ms.keywords: IQueryParserManager, IQueryParserManager interface [search], IQueryParserManager interface [search],described, _search_IQueryParserManager, search._search_IQueryParserManager, structuredquery/IQueryParserManager
f1_keywords:
- structuredquery/IQueryParserManager
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IQueryParserManager interface


## -description


Provides methods to create, initialize, and change options for an <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparser">IQueryParser</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryParserManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryParserManager</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-createloadedparser">CreateLoadedParser</a>
</td>
<td align="left" width="63%">
Creates a new instance of a <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparser">IQueryParser</a> interface implementation. This instance of the query parser is loaded with the schema for the specified catalog and is localized to a specified language. All other settings are initialized to default settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-initializeoptions">InitializeOptions</a>
</td>
<td align="left" width="63%">
Sets the flags for Natural Query Syntax (NQS) and automatic wildcard characters for the specified query parser. If the query parser was created for the <code>SystemIndex</code> catalog, this method also sets up standard condition generators to be used later by the query parser object for recognizing named entities.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-setoption">SetOption</a>
</td>
<td align="left" width="63%">
Changes a single option in this <b>IQueryParserManager</b> object. For example, this method could change the name of the schema binary to load or the location of localized schema binaries.

</td>
</tr>
</table> 


## -remarks



The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/lwef/-search-2x-wds-aqsreference">Advanced Query Syntax</a>
 

 

