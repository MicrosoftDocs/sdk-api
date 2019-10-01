---
UID: NN:structuredquerycondition.ICondition
title: ICondition (structuredquerycondition.h)
author: windows-sdk-content
description: Provides methods for retrieving information about a search condition.
old-location: search\_search_ICondition.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\icondition.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICondition, ICondition interface [search], ICondition interface [search],described, _search_ICondition, search._search_ICondition, structuredquerycondition/ICondition
ms.topic: interface
f1_keywords: 
 - "structuredquerycondition/ICondition"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - ICondition
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# ICondition interface


## -description


Provides methods for retrieving information about a search condition. An <b>ICondition</b> object represents the result of parsing an input string (using methods such as <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-parse">IQueryParser::Parse</a> or <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-getquery">IQuerySolution::GetQuery</a>) into a tree of search condition nodes. A node can be a logical AND, OR, or NOT for comparing subnodes, or it can be a leaf node comparing a property and a constant value.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICondition</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>. <b>ICondition</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a deep copy of this <b>ICondition</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo">GetComparisonInfo</a>
</td>
<td align="left" width="63%">
Retrieves the property name, operation, and value from a leaf search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getconditiontype">GetConditionType</a>
</td>
<td align="left" width="63%">
Retrieves the condition type for this search condition node, identifying it as a logical AND, OR, or NOT, or as a leaf node. 
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms">GetInputTerms</a>
</td>
<td align="left" width="63%">
For a leaf node, <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms">ICondition::GetInputTerms</a> retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions">GetSubConditions</a>
</td>
<td align="left" width="63%">
Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization">GetValueNormalization</a>
</td>
<td align="left" width="63%">
Retrieves the character-normalized value of the search condition node.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype">GetValueType</a>
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




<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>



<b>Reference</b>
 

 

