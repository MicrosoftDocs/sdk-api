---
UID: NN:structuredquery.IQueryParser
title: IQueryParser
author: windows-sdk-content
description: Provides methods to parse an input string into an IQuerySolution object.
old-location: search\_search_IQueryParser.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\iqueryparser.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IQueryParser, IQueryParser interface [search], IQueryParser interface [search],described, _search_IQueryParser, search._search_IQueryParser, structuredquery/IQueryParser
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IQueryParser
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IQueryParser interface


## -description


Provides methods to parse an input string into an <a href="https://msdn.microsoft.com/en-us/library/Bb231346(v=VS.85).aspx">IQuerySolution</a> object.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQueryParser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IQueryParser</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451273">GetOption</a>
</td>
<td align="left" width="63%">
Retrieves a specified simple option value for this query parser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231352(v=VS.85).aspx">GetSchemaProvider</a>
</td>
<td align="left" width="63%">
Retrieves a schema provider for browsing the currently loaded schema.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231354(v=VS.85).aspx">Parse</a>
</td>
<td align="left" width="63%">
Parses an input string that contains Structured Query keywords and/or contents to produce an <a href="https://msdn.microsoft.com/en-us/library/Bb231346(v=VS.85).aspx">IQuerySolution</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231355(v=VS.85).aspx">ParsePropertyValue</a>
</td>
<td align="left" width="63%">
Parses a condition for a specified property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231356(v=VS.85).aspx">RestatePropertyValueToString</a>
</td>
<td align="left" width="63%">
Restates a specified property for a condition as a query string. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231357(v=VS.85).aspx">RestateToString</a>
</td>
<td align="left" width="63%">
Restates a condition as a structured query string. If the condition was the result of parsing an original query string, the keywords of that query string are used to a great extent. If not, default keywords are used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231358(v=VS.85).aspx">SetMultiOption</a>
</td>
<td align="left" width="63%">
Sets a complex option, such as a specified condition generator, to use when parsing an input string. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231359(v=VS.85).aspx">SetOption</a>
</td>
<td align="left" width="63%">
Sets a single option, such as a specified wordbreaker, for parsing an input string.

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965711(v=VS.85).aspx">Advanced Query Syntax</a>
 

 

