---
UID: NF:structuredquery.IConditionFactory2.CreateLeaf
title: IConditionFactory2::CreateLeaf (structuredquery.h)
description: Creates a leaf condition node for any value. The returned object supports ICondition and ICondition2.
helpviewer_keywords: ["CreateLeaf","CreateLeaf method [search]","CreateLeaf method [search]","IConditionFactory2 interface","IConditionFactory2 interface [search]","CreateLeaf method","IConditionFactory2.CreateLeaf","IConditionFactory2::CreateLeaf","_search_IConditionFactory2_CreateLeaf","search._search_IConditionFactory2_CreateLeaf","structuredquery/IConditionFactory2::CreateLeaf"]
old-location: search\_search_IConditionFactory2_CreateLeaf.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\iconditionfactory\createleaf.htm
ms.date: 12/05/2018
ms.keywords: CreateLeaf, CreateLeaf method [search], CreateLeaf method [search],IConditionFactory2 interface, IConditionFactory2 interface [search],CreateLeaf method, IConditionFactory2.CreateLeaf, IConditionFactory2::CreateLeaf, _search_IConditionFactory2_CreateLeaf, search._search_IConditionFactory2_CreateLeaf, structuredquery/IConditionFactory2::CreateLeaf
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
 - IConditionFactory2::CreateLeaf
 - structuredquery/IConditionFactory2::CreateLeaf
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
 - IConditionFactory2.CreateLeaf
---

# IConditionFactory2::CreateLeaf


## -description

Creates a leaf condition node for any value. The returned object supports <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> and <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

The name of the property of the leaf condition as a REFPROPERTYKEY. If the leaf has no particular property, use PKEY_Null.

### -param cop [in]

Type: <b><a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a></b>

A <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a> enumeration. If the leaf has no particular operation, then use <i>COP_IMPLICIT</i>.

### -param propvar [in]

Type: <b>REFPROPERTYKEY</b>

The property value of the leaf condition as a REFPROPERTYKEY.

### -param pszSemanticType [in, optional]

Type: <b>LPCWSTR</b>

The name of a semantic type of the value, or <b>NULL</b> for a plain string. If the newly created leaf is an unresolved named entity, <i>pszSemanticType</i> should be the name of a semantic type, otherwise <b>NULL</b>.

### -param pszLocaleName [in, optional]

Type: <b>LPCWSTR</b>

The name of the locale to be compared, or <b>NULL</b> for an unspecified locale. If <i>propvar</i> does not contain a string value, then <i>pszLocaleName</i> should be LOCALE_NAME_USER_DEFAULT; otherwise, <i>pszLocaleName</i> should reflect the language the string. Alternatively, <i>pszLocaleName</i> could be  LOCALE_NAME_INVARIANT.

### -param pPropertyNameTerm [in, optional]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> that identifies the range of the input string that represents the property. It can be <b>NULL</b>.

### -param pOperationTerm [in, optional]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> that identifies the range of the input string that represents the operation. It can be <b>NULL</b>.

### -param pValueTerm [in, optional]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> that identifies the range of the input string that represents the value. It can be <b>NULL</b>.

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

This method does not return a value.

## -remarks

For default options, use the <i>CONDITION_CREATION_DEFAULT</i> flag.

 If the leaf condition was obtained by parsing a string, one or more of the parameters <i>pPropertyNameTerm</i>, <i>pOperationTerm </i> and <i>pValueTerm</i> may be represented by an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> interface (obtained through the <a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms">ICondition::GetInputTerms</a> method). Otherwise all three parameters can be <b>NULL</b>. 

For more information about leaf node terms (property, value, and operation), see 
<a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms">ICondition::GetInputTerms</a>.

A virtual property has one or more metadata items in which the key is "MapsToRelation" and the value is a property name (which is one expansion of the property). For more information about metadata, see <a href="/windows/desktop/api/structuredquery/nf-structuredquery-irelationship-metadata">MetaData</a>.

## -see-also

<a href="/windows/desktop/api/structuredquery/ne-structuredquery-condition_creation_options">CONDITION_CREATION_OPTIONS</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>