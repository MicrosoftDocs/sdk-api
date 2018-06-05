---
UID: NN:structuredquery.IConditionFactory2
title: IConditionFactory2
author: windows-sdk-content
description: Extends the functionality of IConditionFactory. IConditionFactory2 provides methods for creating or resolving a condition tree that was obtained by parsing a query string.
old-location: search\_search_IConditionFactory2.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\iconditionfactory2.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IConditionFactory2, IConditionFactory2 interface [search], IConditionFactory2 interface [search],described, _search_IConditionFactory2, search._search_IConditionFactory2, structuredquery/IConditionFactory2
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: NAMED_ENTITY_CERTAINTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Structuredquery.h
api_name:
-	IConditionFactory2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionFactory2 interface


## -description


Extends the functionality of <a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>. <b>IConditionFactory2</b> provides methods for creating or resolving a condition tree that was obtained by parsing a query string.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConditionFactory2</b> interface inherits from <a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>. <b>IConditionFactory2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/db321ef5-2838-426b-8402-370ba19a887f">CreateBooleanLeaf</a>
</td>
<td align="left" width="63%">
Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e360e7a3-a54c-4fb3-a34d-0a308b3d99de">CreateCompoundFromArray</a>
</td>
<td align="left" width="63%">

          Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) from an array of condition nodes. The returned object supports             <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d707fbe2-f4c2-4746-985d-dd504d091de0">CreateCompoundFromObjectArray</a>
</td>
<td align="left" width="63%">

          Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) of a collection of subconditions. The returned object supports             <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49ff5cf4-76e9-4ac0-82a2-6ae81c5ddcb1">CreateIntegerLeaf</a>
</td>
<td align="left" width="63%">

          Creates a leaf condition node for an integer value. The returned object supports <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cc17830-4507-4b8d-9b8f-fb9e5ce9dfb6">CreateNegation</a>
</td>
<td align="left" width="63%">

          Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a59bf455-49cb-469a-860d-7ecd7dd94ec0">CreateStringLeaf</a>
</td>
<td align="left" width="63%">

          Creates a leaf condition node for a string value that represents a comparison of property value and constant value. The returned object supports             <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/955df857-a177-4468-8b1d-f0ef3e774067">CreateTrueFalse</a>
</td>
<td align="left" width="63%">
Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7cb9083-4ab9-4550-82e9-5c1da9c0f831">MakeLeaf</a>
</td>
<td align="left" width="63%">

          Creates a leaf condition node for any value. The returned object supports <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61681368-5d27-478b-8063-5c192877a5be">ResolveCondition</a>
</td>
<td align="left" width="63%">
Performs a variety of transformations on a condition tree, and thereby the resolved condition for evaluation. The returned object supports <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>.

</td>
</tr>
</table> 


## -remarks



The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting 
condition trees.




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<b>Reference</b>
 

 

