---
UID: NN:structuredquery.IConditionFactory2
title: IConditionFactory2 (structuredquery.h)
description: Extends the functionality of IConditionFactory. IConditionFactory2 provides methods for creating or resolving a condition tree that was obtained by parsing a query string.
helpviewer_keywords: ["IConditionFactory2","IConditionFactory2 interface [search]","IConditionFactory2 interface [search]","described","_search_IConditionFactory2","search._search_IConditionFactory2","structuredquery/IConditionFactory2"]
old-location: search\_search_IConditionFactory2.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\iconditionfactory2.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory2, IConditionFactory2 interface [search], IConditionFactory2 interface [search],described, _search_IConditionFactory2, search._search_IConditionFactory2, structuredquery/IConditionFactory2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConditionFactory2
 - structuredquery/IConditionFactory2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IConditionFactory2
---

# IConditionFactory2 interface


## -description

Extends the functionality of <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>. <b>IConditionFactory2</b> provides methods for creating or resolving a condition tree that was obtained by parsing a query string.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConditionFactory2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>. <b>IConditionFactory2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createbooleanleaf">CreateBooleanLeaf</a>
</td>
<td align="left" width="63%">
Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createcompoundfromarray">CreateCompoundFromArray</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) from an array of condition nodes. The returned object supports             <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createcompoundfromobjectarray">CreateCompoundFromObjectArray</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) of a collection of subconditions. The returned object supports             <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createintegerleaf">CreateIntegerLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node for an integer value. The returned object supports <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createnegation">CreateNegation</a>
</td>
<td align="left" width="63%">
Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createstringleaf">CreateStringLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node for a string value that represents a comparison of property value and constant value. The returned object supports             <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createtruefalse">CreateTrueFalse</a>
</td>
<td align="left" width="63%">
Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createleaf">MakeLeaf</a>
</td>
<td align="left" width="63%">
Creates a leaf condition node for any value. The returned object supports <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-resolvecondition">ResolveCondition</a>
</td>
<td align="left" width="63%">
Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

</td>
</tr>
</table>

## -remarks

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<b>Reference</b>

