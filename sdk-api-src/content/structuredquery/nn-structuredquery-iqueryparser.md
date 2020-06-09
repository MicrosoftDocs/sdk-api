---
UID: NN:structuredquery.IQueryParser
title: IQueryParser (structuredquery.h)
description: Provides methods to parse an input string into an IQuerySolution object.
helpviewer_keywords: ["IQueryParser","IQueryParser interface [search]","IQueryParser interface [search]","described","_search_IQueryParser","search._search_IQueryParser","structuredquery/IQueryParser"]
old-location: search\_search_IQueryParser.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\iqueryparser.htm
ms.date: 12/05/2018
ms.keywords: IQueryParser, IQueryParser interface [search], IQueryParser interface [search],described, _search_IQueryParser, search._search_IQueryParser, structuredquery/IQueryParser
f1_keywords:
- structuredquery/IQueryParser
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
- IQueryParser
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IQueryParser interface


## -description


Provides methods to parse an input string into an <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> object.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryParser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQueryParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-getoption">GetOption</a>
</td>
<td align="left" width="63%">
Retrieves a specified simple option value for this query parser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-getschemaprovider">GetSchemaProvider</a>
</td>
<td align="left" width="63%">
Retrieves a schema provider for browsing the currently loaded schema.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-parse">Parse</a>
</td>
<td align="left" width="63%">
Parses an input string that contains Structured Query keywords and/or contents to produce an <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-parsepropertyvalue">ParsePropertyValue</a>
</td>
<td align="left" width="63%">
Parses a condition for a specified property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-restatepropertyvaluetostring">RestatePropertyValueToString</a>
</td>
<td align="left" width="63%">
Restates a specified property for a condition as a query string. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-restatetostring">RestateToString</a>
</td>
<td align="left" width="63%">
Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-setmultioption">SetMultiOption</a>
</td>
<td align="left" width="63%">
Sets a complex option, such as a specified condition generator, to use when parsing an input string. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-setoption">SetOption</a>
</td>
<td align="left" width="63%">
Sets a single option, such as a specified wordbreaker, for parsing an input string.

</td>
</tr>
</table> 


## -remarks



The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/lwef/-search-2x-wds-aqsreference">Advanced Query Syntax</a>
 

 

