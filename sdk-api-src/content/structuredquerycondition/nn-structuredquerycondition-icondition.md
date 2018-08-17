---
UID: NN:structuredquerycondition.ICondition
title: ICondition
author: windows-sdk-content
description: Provides methods for retrieving information about a search condition.
old-location: search\_search_ICondition.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\icondition.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICondition, ICondition interface [search], ICondition interface [search],described, _search_ICondition, search._search_ICondition, structuredquerycondition/ICondition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: structuredquerycondition.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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


Provides methods for retrieving information about a search condition. An <b>ICondition</b> object represents the result of parsing an input string (using methods such as <a href="https://msdn.microsoft.com/en-us/library/Bb231354(v=VS.85).aspx">IQueryParser::Parse</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb231345(v=VS.85).aspx">IQuerySolution::GetQuery</a>) into a tree of search condition nodes. A node can be a logical AND, OR, or NOT for comparing subnodes, or it can be a leaf node comparing a property and a constant value.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICondition</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/ms690091(v=VS.85).aspx">IPersistStream</a>. <b>ICondition</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb231388(v=VS.85).aspx">Clone</a>
</td>
<td align="left" width="63%">
Creates a deep copy of this <b>ICondition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231389(v=VS.85).aspx">GetComparisonInfo</a>
</td>
<td align="left" width="63%">
Retrieves the property name, operation, and value from a leaf search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231390(v=VS.85).aspx">GetConditionType</a>
</td>
<td align="left" width="63%">
Retrieves the condition type for this search condition node, identifying it as a logical AND, OR, or NOT, or as a leaf node. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231391(v=VS.85).aspx">GetInputTerms</a>
</td>
<td align="left" width="63%">
For a leaf node, <a href="https://msdn.microsoft.com/en-us/library/Bb231391(v=VS.85).aspx">ICondition::GetInputTerms</a> retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231392(v=VS.85).aspx">GetSubConditions</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231393(v=VS.85).aspx">GetValueNormalization</a>
</td>
<td align="left" width="63%">
Retrieves the character-normalized value of the search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb231394(v=VS.85).aspx">GetValueType</a>
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




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690091(v=VS.85).aspx">IPersistStream</a>



<b>Reference</b>
 

 

