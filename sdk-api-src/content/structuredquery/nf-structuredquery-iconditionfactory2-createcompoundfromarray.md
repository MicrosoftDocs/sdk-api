---
UID: NF:structuredquery.IConditionFactory2.CreateCompoundFromArray
title: IConditionFactory2::CreateCompoundFromArray (structuredquery.h)
description: Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) from an array of condition nodes. The returned object supports ICondition and ICondition2.
helpviewer_keywords: ["CreateCompoundFromArray","CreateCompoundFromArray method [search]","CreateCompoundFromArray method [search]","IConditionFactory2 interface","IConditionFactory2 interface [search]","CreateCompoundFromArray method","IConditionFactory2.CreateCompoundFromArray","IConditionFactory2::CreateCompoundFromArray","_search_IConditionFactory2_CreateCompoundFromArray","search._search_IConditionFactory2_CreateCompoundFromArray","structuredquery/IConditionFactory2::CreateCompoundFromArray"]
old-location: search\_search_IConditionFactory2_CreateCompoundFromArray.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory\createcompoundfromarray.htm
ms.date: 12/05/2018
ms.keywords: CreateCompoundFromArray, CreateCompoundFromArray method [search], CreateCompoundFromArray method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateCompoundFromArray method, IConditionFactory2.CreateCompoundFromArray, IConditionFactory2::CreateCompoundFromArray, _search_IConditionFactory2_CreateCompoundFromArray, search._search_IConditionFactory2_CreateCompoundFromArray, structuredquery/IConditionFactory2::CreateCompoundFromArray
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
 - IConditionFactory2::CreateCompoundFromArray
 - structuredquery/IConditionFactory2::CreateCompoundFromArray
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
 - IConditionFactory2.CreateCompoundFromArray
---

# IConditionFactory2::CreateCompoundFromArray


## -description

Creates a leaf condition node that is a conjunction (AND) or a disjunction (OR) from an array of condition nodes. The returned object supports             <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

## -parameters

### -param ct [in]

Type: <b><a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a></b>

A <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a> enumeration that must be set to either the <i>CT_AND_CONDITION</i> or <i>CT_OR_CONDITION</i> flag.

### -param ppcondSubs [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Each element of the <i>ppCondSubs</i> parameter must implement <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>.

### -param cSubs [in]

Type: <b>ULONG</b>

The leaf subcondition as an unsigned 64-bit integer value.

### -param cco [in]

Type: <b><a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a> enumeration.

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>, IID_IEnumVARIANT, or (for a negation condition) IID_ICondition.

### -param ppv [out]

Type: <b>void**</b>

A collection of zero or more <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a> objects.

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