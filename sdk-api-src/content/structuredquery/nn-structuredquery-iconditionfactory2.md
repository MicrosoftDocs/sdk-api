---
UID: NN:structuredquery.IConditionFactory2
title: IConditionFactory2 (structuredquery.h)
author: windows-sdk-content
description: Extends the functionality of IConditionFactory. IConditionFactory2 provides methods for creating or resolving a condition tree that was obtained by parsing a query string.
old-location: search\_search_IConditionFactory2.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\iconditionfactory2.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IConditionFactory2, IConditionFactory2 interface [search], IConditionFactory2 interface [search],described, _search_IConditionFactory2, search._search_IConditionFactory2, structuredquery/IConditionFactory2
ms.topic: interface
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IConditionFactory2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConditionFactory2 interface


## -description


Extends the functionality of <a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>. <b>IConditionFactory2</b> provides methods for creating or resolving a condition tree that was obtained by parsing a query string.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConditionFactory2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>. <b>IConditionFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConditionFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742794(v=VS.85).aspx">CreateBooleanLeaf</a>
</td>
<td align="left" width="63%">
Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742801(v=VS.85).aspx">CreateCompoundFromArray</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) from an array of condition nodes. The returned object supports             <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742793(v=VS.85).aspx">CreateCompoundFromObjectArray</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) of a collection of subconditions. The returned object supports             <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742795(v=VS.85).aspx">CreateIntegerLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node for an integer value. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742796(v=VS.85).aspx">CreateNegation</a>
</td>
<td align="left" width="63%">
Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742797(v=VS.85).aspx">CreateStringLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node for a string value that represents a comparison of property value and constant value. The returned object supports             <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742798(v=VS.85).aspx">CreateTrueFalse</a>
</td>
<td align="left" width="63%">
Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742802(v=VS.85).aspx">MakeLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node for any value. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd742800(v=VS.85).aspx">ResolveCondition</a>
</td>
<td align="left" width="63%">
Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>.

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting 
condition trees.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd797838(v=VS.85).aspx">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>



<b>Reference</b>
 

 

