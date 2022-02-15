---
UID: NF:structuredquery.IConditionFactory.MakeLeaf
title: IConditionFactory::MakeLeaf (structuredquery.h)
description: Creates a leaf condition node that represents a comparison of property value and constant value.
helpviewer_keywords: ["IConditionFactory interface [search]","MakeLeaf method","IConditionFactory.MakeLeaf","IConditionFactory::MakeLeaf","MakeLeaf","MakeLeaf method [search]","MakeLeaf method [search]","IConditionFactory interface","_search_IConditionFactory_MakeLeaf","search._search_IConditionFactory_MakeLeaf","structuredquery/IConditionFactory::MakeLeaf"]
old-location: search\_search_IConditionFactory_MakeLeaf.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\makeleaf.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory interface [search],MakeLeaf method, IConditionFactory.MakeLeaf, IConditionFactory::MakeLeaf, MakeLeaf, MakeLeaf method [search], MakeLeaf method [search],IConditionFactory interface, _search_IConditionFactory_MakeLeaf, search._search_IConditionFactory_MakeLeaf, structuredquery/IConditionFactory::MakeLeaf
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
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - IConditionFactory::MakeLeaf
 - structuredquery/IConditionFactory::MakeLeaf
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
 - IConditionFactory.MakeLeaf
---

# IConditionFactory::MakeLeaf


## -description

Creates a leaf condition node that represents a comparison of property value and constant value.

## -parameters

### -param pszPropertyName [in]

Type: <b>LPCWSTR</b>

The name of a property to be compared, or <b>NULL</b> for an unspecified property. The locale name of the leaf node is LOCALE_NAME_USER_DEFAULT.

### -param cop [in]

Type: <b><a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a></b>

A <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a> enumeration.

### -param pszValueType [in]

Type: <b>LPCWSTR</b>

The name of a semantic type of the value, or <b>NULL</b> for a plain string.

### -param ppropvar [in]

Type: <b>PROPVARIANT const*</b>

The constant value against which the property value should be compared.

### -param pPropertyNameTerm [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> that identifies the range of the input string that represents the property. It can be <b>NULL</b>.

### -param pOperationTerm [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> that identifies the range of the input string that represents the operation. It can be <b>NULL</b>.

### -param pValueTerm [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> that identifies the range of the input string that represents the value. It can be <b>NULL</b>.

### -param fExpand [in]

Type: <b>BOOL</b>

If <b>TRUE</b> and <i>pszPropertyName</i> identifies a virtual property, the resulting node is not a leaf node; instead, it is a disjunction of leaf condition nodes, each of which corresponds to one expansion of the virtual property.

### -param ppcResult [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Receives a pointer to the new <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> leaf node.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about leaf node terms (property, value, and operation), see 
<a href="/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms">ICondition::GetInputTerms</a>.

A virtual property has one or more metadata items in which the key is "MapsToRelation" and the value is a property name (which is one expansion of the property). For more information about metadata, see <a href="/windows/desktop/api/structuredquery/nf-structuredquery-irelationship-metadata">MetaData</a>.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>