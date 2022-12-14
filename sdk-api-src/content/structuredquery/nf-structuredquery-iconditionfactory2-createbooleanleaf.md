---
UID: NF:structuredquery.IConditionFactory2.CreateBooleanLeaf
title: IConditionFactory2::CreateBooleanLeaf (structuredquery.h)
description: Creates a search condition that is either TRUE or FALSE. (IConditionFactory2.CreateBooleanLeaf)
helpviewer_keywords: ["CreateBooleanLeaf","CreateBooleanLeaf method [search]","CreateBooleanLeaf method [search]","IConditionFactory2 interface","IConditionFactory2 interface [search]","CreateBooleanLeaf method","IConditionFactory2.CreateBooleanLeaf","IConditionFactory2::CreateBooleanLeaf","_search_IConditionFactory2_CreateBooleanLeaf","search._search_IConditionFactory2_CreateBooleanLeaf","structuredquery/IConditionFactory2::CreateBooleanLeaf"]
old-location: search\_search_IConditionFactory2_CreateBooleanLeaf.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\createbooleanleaf.htm
ms.date: 12/05/2018
ms.keywords: CreateBooleanLeaf, CreateBooleanLeaf method [search], CreateBooleanLeaf method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateBooleanLeaf method, IConditionFactory2.CreateBooleanLeaf, IConditionFactory2::CreateBooleanLeaf, _search_IConditionFactory2_CreateBooleanLeaf, search._search_IConditionFactory2_CreateBooleanLeaf, structuredquery/IConditionFactory2::CreateBooleanLeaf
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConditionFactory2::CreateBooleanLeaf
 - structuredquery/IConditionFactory2::CreateBooleanLeaf
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
 - IConditionFactory2.CreateBooleanLeaf
---

# IConditionFactory2::CreateBooleanLeaf


## -description

Creates a search condition that is either <b>TRUE</b> or <b>FALSE</b>. The returned object supports <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The name of the property of the leaf condition as a REFPROPERTYKEY. If the leaf has no particular property, use PKEY_Null.

### -param cop [in]

Type: <b><a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a></b>

A <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a> enumeration. If the leaf has no particular operation, then use <i>COP_IMPLICIT</i>.

### -param fValue [in]

Type: <b>BOOL</b>

The value of the search condition to use. <i>fValue</i> should typically be set to VARIANT_FALSE.

### -param cco [in]

Type: <b><a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a> enumeration.

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>, <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>, or (for a negation condition) IID_ICondition.

### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a> objects.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For default options, use the <i>CONDITION_CREATION_DEFAULT</i> flag.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>
