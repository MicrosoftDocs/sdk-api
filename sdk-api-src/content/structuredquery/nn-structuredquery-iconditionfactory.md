---
UID: NN:structuredquery.IConditionFactory
title: IConditionFactory (structuredquery.h)
description: Provides methods for creating or resolving a condition tree that was obtained by parsing a query string.
old-location: search\_search_IConditionFactory.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\iconditionfactory.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory, IConditionFactory interface [search], IConditionFactory interface [search],described, _search_IConditionFactory, search._search_IConditionFactory, structuredquery/IConditionFactory
f1_keywords:
- structuredquery/IConditionFactory
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
- IConditionFactory
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# IConditionFactory interface


## -description


Provides methods for creating or resolving a condition tree that was obtained by parsing a query string.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConditionFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConditionFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConditionFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-makeandor">MakeAndOr</a>
</td>
<td align="left" width="63%">
Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-makeleaf">MakeLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node that represents a comparison of property value and constant value.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-makenot">MakeNot</a>
</td>
<td align="left" width="63%">
Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory-resolve">Resolve</a>
</td>
<td align="left" width="63%">
Performs a variety of transformations on a condition tree, including the following: resolves conditions with relative date/time expressions to conditions with absolute date/time (as a VT_FILETIME); turns other recognized named entities into condition trees with actual values; simplifies condition trees; replaces virtual or compound properties with OR trees of other properties; removes condition trees resulting from queries with property keywords that had no condition applied.

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="https://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="https://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>
 

 

