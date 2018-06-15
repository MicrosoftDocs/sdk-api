---
UID: NF:structuredquery.IConditionFactory2.CreateBooleanLeaf
title: IConditionFactory2::CreateBooleanLeaf
author: windows-sdk-content
description: Creates a search condition that is either TRUE or FALSE.
old-location: search\_search_IConditionFactory2_CreateBooleanLeaf.htm
old-project: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\createbooleanleaf.htm
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: CreateBooleanLeaf, CreateBooleanLeaf method [search], CreateBooleanLeaf method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateBooleanLeaf method, IConditionFactory2.CreateBooleanLeaf, IConditionFactory2::CreateBooleanLeaf, _search_IConditionFactory2_CreateBooleanLeaf, search._search_IConditionFactory2_CreateBooleanLeaf, structuredquery/IConditionFactory2::CreateBooleanLeaf
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquery.h
api_name:
 - IConditionFactory2.CreateBooleanLeaf
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IConditionFactory2::CreateBooleanLeaf


## -description


Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The name of the property of the leaf condition as a REFPROPERTYKEY. If the leaf has no particular property, use PKEY_Null.


### -param cop [in]

Type: <b><a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a></b>

A <a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a> enumeration. If the leaf has no particular operation, then use <i>COP_IMPLICIT</i>.


### -param fValue [in]

Type: <b>BOOL</b>

The value of the search condition to use. <i>fValue</i> should typically be set to VARIANT_FALSE.


### -param cco [in]

Type: <b><a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a> enumeration.


### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>, or (for a negation condition) IID_ICondition.


### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a> and <a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a> objects.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For default options, use the <i>CONDITION_CREATION_DEFAULT</i> flag.




## -see-also




<a href="https://msdn.microsoft.com/5fa88dc1-8ca3-4247-8bad-bba8be2ad734">CONDITION_CREATION_OPTIONS</a>



<a href="https://msdn.microsoft.com/d1ec553d-f9fb-4039-9121-0f57bac15345">CONDITION_OPERATION</a>



<a href="https://msdn.microsoft.com/921cdcb0-2915-4bbe-af4b-3f62c3867ea4">CONDITION_TYPE</a>



<a href="https://msdn.microsoft.com/7b880393-699d-438d-8d45-08fffc9d482f">ICondition</a>



<a href="https://msdn.microsoft.com/32c68ff7-f0f3-40eb-801a-c5c21ec496fa">ICondition2</a>



<a href="https://msdn.microsoft.com/c678fa37-8673-4da7-9c23-9a7f478dc1b0">IConditionFactory</a>



<a href="https://msdn.microsoft.com/5ac0acb1-67f0-43f0-b1c1-2d8cf682a277">IConditionFactory2</a>



<b>Reference</b>
 

 

