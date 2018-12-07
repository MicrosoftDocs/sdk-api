---
UID: NN:structuredquery.IConditionFactory
title: IConditionFactory
author: windows-sdk-content
description: Provides methods for creating or resolving a condition tree that was obtained by parsing a query string.
old-location: search\_search_IConditionFactory.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\iconditionfactory.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IConditionFactory, IConditionFactory interface [search], IConditionFactory interface [search],described, _search_IConditionFactory, search._search_IConditionFactory, structuredquery/IConditionFactory
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IConditionFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# IConditionFactory interface


## -description


Provides methods for creating or resolving a condition tree that was obtained by parsing a query string.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConditionFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IConditionFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb231384(v=VS.85).aspx">MakeAndOr</a>
</td>
<td align="left" width="63%">
Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231385(v=VS.85).aspx">MakeLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node that represents a comparison of property value and constant value.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231386(v=VS.85).aspx">MakeNot</a>
</td>
<td align="left" width="63%">
Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231387(v=VS.85).aspx">Resolve</a>
</td>
<td align="left" width="63%">
Performs a variety of transformations on a condition tree, including the following: resolves conditions with relative date/time expressions to conditions with absolute date/time (as a VT_FILETIME); turns other recognized named entities into condition trees with actual values; simplifies condition trees; replaces virtual or compound properties with OR trees of other properties; removes condition trees resulting from queries with property keywords that had no condition applied.

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742799(v=VS.85).aspx">IConditionFactory2</a>



<b>Reference</b>
 

 

