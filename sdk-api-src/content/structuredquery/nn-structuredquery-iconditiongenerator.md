---
UID: NN:structuredquery.IConditionGenerator
title: IConditionGenerator (structuredquery.h)
description: Provides methods for handling named entities and generating special conditions.
helpviewer_keywords: ["IConditionGenerator","IConditionGenerator interface [search]","IConditionGenerator interface [search]","described","_search_IConditionGenerator","search._search_IConditionGenerator","structuredquery/IConditionGenerator"]
old-location: search\_search_IConditionGenerator.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditiongenerator\iconditiongenerator.htm
ms.date: 12/05/2018
ms.keywords: IConditionGenerator, IConditionGenerator interface [search], IConditionGenerator interface [search],described, _search_IConditionGenerator, search._search_IConditionGenerator, structuredquery/IConditionGenerator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConditionGenerator
 - structuredquery/IConditionGenerator
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
 - IConditionGenerator
---

# IConditionGenerator interface


## -description

Provides methods for handling named entities and generating special conditions.

## -inheritance

The <b>IConditionGenerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IConditionGenerator</b> also has these types of members:

## -remarks

When an object that supports <b>IConditionGenerator</b> has been registered with a query parser as a semantic type T (using the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-setmultioption">IQueryParser::SetMultiOption</a> method with the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_multioption">SQMO_GENERATOR_FOR_TYPE</a> constant), and that query parser is about to generate a leaf condition node with semantic type T, the query parser first calls the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf">IConditionGenerator::GenerateForLeaf</a> method of the condition generator. If that method returns S_OK, the returned condition tree (which need not be a leaf node) is used. If it returns S_FALSE, then normal processing ia resumed, which generates a leaf node.

A query parser has condition generators preregistered for the known semantic types representing numbers, Booleans, date/time and file paths.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<b>Reference</b>
