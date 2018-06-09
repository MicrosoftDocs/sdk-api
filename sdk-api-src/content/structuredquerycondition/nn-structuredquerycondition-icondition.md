---
UID: NN:structuredquerycondition.ICondition
title: ICondition
author: windows-sdk-content
description: Provides methods for retrieving information about a search condition.
old-location: search\_search_ICondition.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\icondition.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ICondition, ICondition interface [search], ICondition interface [search],described, _search_ICondition, search._search_ICondition, structuredquerycondition/ICondition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquerycondition.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CONDITION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - ICondition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ICondition interface


## -description


Provides methods for retrieving information about a search condition. An <b>ICondition</b> object represents the result of parsing an input string (using methods such as <a href="https://msdn.microsoft.com/2ca6ddfa-821c-4d84-abbf-61d25b633180">IQueryParser::Parse</a> or <a href="https://msdn.microsoft.com/ef03828a-ac31-4e73-a8bb-44f0b1963107">IQuerySolution::GetQuery</a>) into a tree of search condition nodes. A node can be a logical AND, OR, or NOT for comparing subnodes, or it can be a leaf node comparing a property and a constant value.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICondition</b> interface inherits from <a href="_com_IPersistStream">IPersistStream</a>. <b>ICondition</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICondition</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">

      Creates a deep copy of this <b>ICondition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b87aa9dd-afed-4fe4-83e2-2a04d8ef2f0c">GetComparisonInfo</a>
</td>
<td align="left" width="63%">

          Retrieves the property name, operation, and value from a leaf search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba2a2fa0-7d1e-4009-9c93-f620cc691b44">GetConditionType</a>
</td>
<td align="left" width="63%">

          Retrieves the condition type for this search condition node, identifying it as a logical AND, OR, or NOT, or as a leaf node. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d169fb4-177f-42e6-a24c-bb0052d1d62b">GetInputTerms</a>
</td>
<td align="left" width="63%">
For a leaf node, <a href="https://msdn.microsoft.com/9d169fb4-177f-42e6-a24c-bb0052d1d62b">ICondition::GetInputTerms</a> retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e65e634d-8c55-4706-ae88-123c735f3594">GetSubConditions</a>
</td>
<td align="left" width="63%">

            Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96c0296e-6828-4cc7-83ab-7719bdc6edfe">GetValueNormalization</a>
</td>
<td align="left" width="63%">

          Retrieves the character-normalized value of the search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cde4e96e-a5e7-4469-aa31-59559832c56e">GetValueType</a>
</td>
<td align="left" width="63%">

          Retrieves the semantic type of the value of the search condition node.
        

</td>
</tr>
</table> 


## -remarks



Prior to Windows 7, this interface was only declared in structuredquery.h and structuredquery.idl. In Windows 7, this interface is also defined in structuredquerycondition.idl and structuredquerycondition.h.

The StructuredQuerySample code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="_com_IPersistStream">IPersistStream</a>



<b>Reference</b>
 

 

