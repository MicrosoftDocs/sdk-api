---
UID: NN:structuredquery.IConditionGenerator
title: IConditionGenerator (structuredquery.h)
description: Provides methods for handling named entities and generating special conditions.
old-location: search\_search_IConditionGenerator.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\iconditiongenerator.htm
ms.date: 12/05/2018
ms.keywords: IConditionGenerator, IConditionGenerator interface [search], IConditionGenerator interface [search],described, _search_IConditionGenerator, search._search_IConditionGenerator, structuredquery/IConditionGenerator
f1_keywords:
- structuredquery/IConditionGenerator
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
- IConditionGenerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IConditionGenerator interface


## -description


Provides methods for handling named entities and generating special conditions.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConditionGenerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConditionGenerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConditionGenerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-defaultphrase">DefaultPhrase</a>
</td>
<td align="left" width="63%">
This method attempts to produce a phrase that, when recognized by this instance of <b>IConditionGenerator</b>, represents the type and value pair for an entity, relationship, or named entity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">GenerateForLeaf</a>
</td>
<td align="left" width="63%">
Generates a special query expression for what would otherwise become a leaf query expression.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Resets all states of the interface to default values and retrieves any necessary information from the schema.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities">RecognizeNamedEntities</a>
</td>
<td align="left" width="63%">
Identifies named entities in an input string, and creates a collection containing them. The value of each named entity is expressed as a string, which is then used by <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">IConditionGenerator::GenerateForLeaf</a>. The string can contain any data and be in any format, because it is not examined by any other components.
	    

</td>
</tr>
</table> 


## -remarks



When an object that supports <b>IConditionGenerator</b> has been registered with a query parser as a semantic type T (using the <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-setmultioption">IQueryParser::SetMultiOption</a> method with the <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_multioption">SQMO_GENERATOR_FOR_TYPE</a> constant), and that query parser is about to generate a leaf condition node with semantic type T, the query parser first calls the <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">IConditionGenerator::GenerateForLeaf</a> method of the condition generator. If that method returns S_OK, the returned condition tree (which need not be a leaf node) is used. If it returns S_FALSE, then normal processing ia resumed, which generates a leaf node.

A query parser has condition generators preregistered for the known semantic types representing numbers, Booleans, date/time and file paths.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<b>Reference</b>
 

 

