---
UID: NN:structuredquery.IQuerySolution
title: IQuerySolution (structuredquery.h)
description: Provides methods that retrieve information about the interpretation of a parsed query.helpviewer_keywords: ["IQuerySolution","IQuerySolution interface [search]","IQuerySolution interface [search]","described","_search_IQuerySolution","search._search_IQuerySolution","structuredquery/IQuerySolution"]
old-location: search\_search_IQuerySolution.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iquerysolution\iquerysolution.htm
ms.date: 12/05/2018
ms.keywords: IQuerySolution, IQuerySolution interface [search], IQuerySolution interface [search],described, _search_IQuerySolution, search._search_IQuerySolution, structuredquery/IQuerySolution
f1_keywords:
- structuredquery/IQuerySolution
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
- IQuerySolution
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IQuerySolution interface


## -description


Provides methods that retrieve information about the interpretation of a parsed query.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQuerySolution</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>. <b>IQuerySolution</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQuerySolution</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-geterrors">GetErrors</a>
</td>
<td align="left" width="63%">
Identifies parts of the input string that the parser did not recognize or did not use when constructing the <b>IQuerySolution</b> condition tree.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-getlexicaldata">GetLexicalData</a>
</td>
<td align="left" width="63%">
Reports the query string, how it was tokenized, and what LCID and word breaker were used to parse it.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-getquery">GetQuery</a>
</td>
<td align="left" width="63%">
Retrieves the condition tree and the semantic type of the solution.
        

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="https://code.msdn.microsoft.com/windowssearch">Code Gallery</a> and the <a href="https://msdn.microsoft.com/windowsvista/bb980924.aspx">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.



