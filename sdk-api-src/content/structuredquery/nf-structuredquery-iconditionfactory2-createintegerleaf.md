---
UID: NF:structuredquery.IConditionFactory2.CreateIntegerLeaf
title: IConditionFactory2::CreateIntegerLeaf (structuredquery.h)
description: Creates a leaf condition node for an integer value. The returned object supports ICondition and ICondition2.
helpviewer_keywords: ["CreateIntegerLeaf","CreateIntegerLeaf method [search]","CreateIntegerLeaf method [search]","IConditionFactory2 interface","IConditionFactory2 interface [search]","CreateIntegerLeaf method","IConditionFactory2.CreateIntegerLeaf","IConditionFactory2::CreateIntegerLeaf","_search_IConditionFactory2_CreateIntegerLeaf","search._search_IConditionFactory2_CreateIntegerLeaf","structuredquery/IConditionFactory2::CreateIntegerLeaf"]
old-location: search\_search_IConditionFactory2_CreateIntegerLeaf.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory2\createintegerleaf.htm
ms.date: 12/05/2018
ms.keywords: CreateIntegerLeaf, CreateIntegerLeaf method [search], CreateIntegerLeaf method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateIntegerLeaf method, IConditionFactory2.CreateIntegerLeaf, IConditionFactory2::CreateIntegerLeaf, _search_IConditionFactory2_CreateIntegerLeaf, search._search_IConditionFactory2_CreateIntegerLeaf, structuredquery/IConditionFactory2::CreateIntegerLeaf
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
 - IConditionFactory2::CreateIntegerLeaf
 - structuredquery/IConditionFactory2::CreateIntegerLeaf
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
 - IConditionFactory2.CreateIntegerLeaf
---

# IConditionFactory2::CreateIntegerLeaf


## -description

Creates a leaf condition node for an integer value. The returned object supports <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The name of the property of the leaf condition as a REFPROPERTYKEY. If the leaf has no particular property, use PKEY_Null.

### -param cop [in]

Type: <b><a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a></b>

A <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a> enumeration. If the leaf has no particular operation, then use <i>COP_IMPLICIT</i>.

### -param lValue [in]

Type: <b>INT32</b>

The value of a leaf condition node as a 32-bit integer.

### -param cco [in]

Type: <b><a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a></b>

The condition creation operation of the leaf condition as the <a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a> enumeration.

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>, IID_IEnumVARIANT, or (for a negation condition) IID_ICondition.

### -param ppv [out]

Type: <b>void**</b>

Receives a pointer to zero or more <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a> objects.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

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