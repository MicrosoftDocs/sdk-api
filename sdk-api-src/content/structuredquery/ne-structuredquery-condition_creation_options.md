---
UID: NE:structuredquery.CONDITION_CREATION_OPTIONS
title: CONDITION_CREATION_OPTIONS
author: windows-driver-content
description: Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node:\_ICondition, ICondition2, IConditionFactory, IConditionFactory2, and IConditionGenerator.
old-location: search\_search_CONDITION_CREATION_OPTIONS.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\condition_creation_options.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: CONDITION_CREATION_DEFAULT, CONDITION_CREATION_NONE, CONDITION_CREATION_OPTIONS, CONDITION_CREATION_OPTIONS enumeration [search], CONDITION_CREATION_SIMPLIFY, CONDITION_CREATION_USE_CONTENT_LOCALE, CONDITION_CREATION_VECTOR_AND, CONDITION_CREATION_VECTOR_LEAF, CONDITION_CREATION_VECTOR_OR, _search_CONDITION_CREATION_OPTIONS, search._search_CONDITION_CREATION_OPTIONS, structuredquery/CONDITION_CREATION_DEFAULT, structuredquery/CONDITION_CREATION_NONE, structuredquery/CONDITION_CREATION_OPTIONS, structuredquery/CONDITION_CREATION_SIMPLIFY, structuredquery/CONDITION_CREATION_USE_CONTENT_LOCALE, structuredquery/CONDITION_CREATION_VECTOR_AND, structuredquery/CONDITION_CREATION_VECTOR_LEAF, structuredquery/CONDITION_CREATION_VECTOR_OR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnalignedStringCchLengthW (Unicode) and StringCchLengthA (ANSI)
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CONDITION_CREATION_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Structuredquery.h
api_name:
-	CONDITION_CREATION_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# CONDITION_CREATION_OPTIONS enumeration


## -description


Provides a set of flags to be used with the following interfaces to indicate the type of condition tree node: <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>, 
<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>, <a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>, <a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>, and <a href="https://msdn.microsoft.com/30fa2fb6-7dfd-41e1-ab4f-5fd80c8a81ec">IConditionGenerator</a>.


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

Indicates that you should ignore any specified locale and use the currently selected content locale <a href="https://msdn.microsoft.com/a59bf455-49cb-469a-860d-7ecd7dd94ec0">IConditionFactory2::CreateStringLeaf</a> and <a href="https://msdn.microsoft.com/e7cb9083-4ab9-4550-82e9-5c1da9c0f831">IConditionFactory2::CreateLeaf</a>.


## -remarks



&gt;Only one of following flags should be set simultaneously:
                

<ul>
<li>CONDITION_CREATION_VECTOR_AND</li>
<li>CONDITION_CREATION_VECTOR_OR</li>
<li>CONDITION_CREATION_VECTOR_LEAF</li>
</ul>
However, if none of these flags is set, then attempting to create a leaf condition with VT_VECTOR set in the PROPVARIANT results in failure.




## -see-also




<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<b>Reference</b>
 

 

