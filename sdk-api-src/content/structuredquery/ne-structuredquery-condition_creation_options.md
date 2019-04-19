---
UID: NE:structuredquery.CONDITION_CREATION_OPTIONS
title: CONDITION_CREATION_OPTIONS (structuredquery.h)
author: windows-sdk-content
description: Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node:\_ICondition, ICondition2, IConditionFactory, IConditionFactory2, and IConditionGenerator.
old-location: search\_search_CONDITION_CREATION_OPTIONS.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\condition_creation_options.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CONDITION_CREATION_DEFAULT, CONDITION_CREATION_NONE, CONDITION_CREATION_OPTIONS, CONDITION_CREATION_OPTIONS enumeration [search], CONDITION_CREATION_SIMPLIFY, CONDITION_CREATION_USE_CONTENT_LOCALE, CONDITION_CREATION_VECTOR_AND, CONDITION_CREATION_VECTOR_LEAF, CONDITION_CREATION_VECTOR_OR, _search_CONDITION_CREATION_OPTIONS, search._search_CONDITION_CREATION_OPTIONS, structuredquery/CONDITION_CREATION_DEFAULT, structuredquery/CONDITION_CREATION_NONE, structuredquery/CONDITION_CREATION_OPTIONS, structuredquery/CONDITION_CREATION_SIMPLIFY, structuredquery/CONDITION_CREATION_USE_CONTENT_LOCALE, structuredquery/CONDITION_CREATION_VECTOR_AND, structuredquery/CONDITION_CREATION_VECTOR_LEAF, structuredquery/CONDITION_CREATION_VECTOR_OR
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: CONDITION_CREATION_OPTIONS
req.redist: 
ms.custom: 19H1
---

# CONDITION_CREATION_OPTIONS enumeration


## -description


Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node: <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a>, 
<a href="https://msdn.microsoft.com/en-us/library/Dd742811(v=VS.85).aspx">ICondition2</a>, <a href="https://msdn.microsoft.com/en-us/library/Bb231383(v=VS.85).aspx">IConditionFactory</a>, <a href="https://msdn.microsoft.com/en-us/library/Dd742799(v=VS.85).aspx">IConditionFactory2</a>, and <a href="https://msdn.microsoft.com/en-us/library/Bb231380(v=VS.85).aspx">IConditionGenerator</a>.


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

Indicates that you should ignore any specified locale and use the currently selected content locale <a href="https://msdn.microsoft.com/en-us/library/Dd742797(v=VS.85).aspx">IConditionFactory2::CreateStringLeaf</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd742802(v=VS.85).aspx">IConditionFactory2::CreateLeaf</a>.


## -remarks



&gt;Only one of following flags should be set simultaneously:
                

<ul>
<li>CONDITION_CREATION_VECTOR_AND</li>
<li>CONDITION_CREATION_VECTOR_OR</li>
<li>CONDITION_CREATION_VECTOR_LEAF</li>
</ul>
However, if none of these flags is set, then attempting to create a leaf condition with VT_VECTOR set in the PROPVARIANT results in failure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965691(v=VS.85).aspx">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965692(v=VS.85).aspx">CONDITION_TYPE</a>



<b>Reference</b>
 

 

