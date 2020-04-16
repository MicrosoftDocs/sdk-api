---
UID: NE:structuredquery.CONDITION_CREATION_OPTIONS
title: CONDITION_CREATION_OPTIONS (structuredquery.h)
description: Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node:\_ICondition, ICondition2, IConditionFactory, IConditionFactory2, and IConditionGenerator.helpviewer_keywords: ["CONDITION_CREATION_DEFAULT","CONDITION_CREATION_NONE","CONDITION_CREATION_OPTIONS","CONDITION_CREATION_OPTIONS enumeration [search]","CONDITION_CREATION_SIMPLIFY","CONDITION_CREATION_USE_CONTENT_LOCALE","CONDITION_CREATION_VECTOR_AND","CONDITION_CREATION_VECTOR_LEAF","CONDITION_CREATION_VECTOR_OR","_search_CONDITION_CREATION_OPTIONS","search._search_CONDITION_CREATION_OPTIONS","structuredquery/CONDITION_CREATION_DEFAULT","structuredquery/CONDITION_CREATION_NONE","structuredquery/CONDITION_CREATION_OPTIONS","structuredquery/CONDITION_CREATION_SIMPLIFY","structuredquery/CONDITION_CREATION_USE_CONTENT_LOCALE","structuredquery/CONDITION_CREATION_VECTOR_AND","structuredquery/CONDITION_CREATION_VECTOR_LEAF","structuredquery/CONDITION_CREATION_VECTOR_OR"]
old-location: search\_search_CONDITION_CREATION_OPTIONS.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\condition_creation_options.htm
ms.date: 12/05/2018
ms.keywords: CONDITION_CREATION_DEFAULT, CONDITION_CREATION_NONE, CONDITION_CREATION_OPTIONS, CONDITION_CREATION_OPTIONS enumeration [search], CONDITION_CREATION_SIMPLIFY, CONDITION_CREATION_USE_CONTENT_LOCALE, CONDITION_CREATION_VECTOR_AND, CONDITION_CREATION_VECTOR_LEAF, CONDITION_CREATION_VECTOR_OR, _search_CONDITION_CREATION_OPTIONS, search._search_CONDITION_CREATION_OPTIONS, structuredquery/CONDITION_CREATION_DEFAULT, structuredquery/CONDITION_CREATION_NONE, structuredquery/CONDITION_CREATION_OPTIONS, structuredquery/CONDITION_CREATION_SIMPLIFY, structuredquery/CONDITION_CREATION_USE_CONTENT_LOCALE, structuredquery/CONDITION_CREATION_VECTOR_AND, structuredquery/CONDITION_CREATION_VECTOR_LEAF, structuredquery/CONDITION_CREATION_VECTOR_OR
f1_keywords:
- structuredquery/CONDITION_CREATION_OPTIONS
dev_langs:
- c++
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
- HeaderDef
api_location:
- Structuredquery.h
api_name:
- CONDITION_CREATION_OPTIONS
targetos: Windows
req.typenames: CONDITION_CREATION_OPTIONS
req.redist: 
ms.custom: 19H1
---

# CONDITION_CREATION_OPTIONS enumeration


## -description


Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node: <a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>, <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>, <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a>.


## -enum-fields




### -field CONDITION_CREATION_DEFAULT

Indicates that the condition is set to the default value.


### -field CONDITION_CREATION_NONE

Indicates that the condition is set to <b>NULL</b>.


### -field CONDITION_CREATION_SIMPLIFY

Indicates that you should simplify the returned condition as much as possible. In some cases this flag indicates that the returned condition is not newly created but refers to an existing object.


### -field CONDITION_CREATION_VECTOR_AND

Indicates that you should create an AND condition of leaves with vector elements as values, instead of attempting to create a leaf condition with VT_VECTOR set in the PROPVARIANT.


### -field CONDITION_CREATION_VECTOR_OR

Indicates that you should create an OR condition of leaves with vector elements as values, instead of attempting to create a leaf condition with VT_VECTOR set in the PROPVARIANT.


### -field CONDITION_CREATION_VECTOR_LEAF

Indicates that you should allow the creation of a leaf condition with VT_VECTOR set in the PROPVARIANT.


### -field CONDITION_CREATION_USE_CONTENT_LOCALE

Indicates that you should ignore any specified locale and use the currently selected content locale <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createstringleaf">IConditionFactory2::CreateStringLeaf</a> and <a href="https://docs.microsoft.com/windows/desktop/api/structuredquery/nf-structuredquery-iconditionfactory2-createleaf">IConditionFactory2::CreateLeaf</a>.


## -remarks



&gt;Only one of following flags should be set simultaneously:
                

<ul>
<li>CONDITION_CREATION_VECTOR_AND</li>
<li>CONDITION_CREATION_VECTOR_OR</li>
<li>CONDITION_CREATION_VECTOR_LEAF</li>
</ul>
However, if none of these flags is set, then attempting to create a leaf condition with VT_VECTOR set in the PROPVARIANT results in failure.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="https://docs.microsoft.com/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<b>Reference</b>
 

 

