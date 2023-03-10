---
UID: NF:structuredquery.IConditionFactory.MakeAndOr
title: IConditionFactory::MakeAndOr (structuredquery.h)
description: Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions.
helpviewer_keywords: ["IConditionFactory interface [search]","MakeAndOr method","IConditionFactory.MakeAndOr","IConditionFactory::MakeAndOr","MakeAndOr","MakeAndOr method [search]","MakeAndOr method [search]","IConditionFactory interface","_search_IConditionFactory_MakeAndOr","search._search_IConditionFactory_MakeAndOr","structuredquery/IConditionFactory::MakeAndOr"]
old-location: search\_search_IConditionFactory_MakeAndOr.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\makeandor.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory interface [search],MakeAndOr method, IConditionFactory.MakeAndOr, IConditionFactory::MakeAndOr, MakeAndOr, MakeAndOr method [search], MakeAndOr method [search],IConditionFactory interface, _search_IConditionFactory_MakeAndOr, search._search_IConditionFactory_MakeAndOr, structuredquery/IConditionFactory::MakeAndOr
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
 - IConditionFactory::MakeAndOr
 - structuredquery/IConditionFactory::MakeAndOr
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
 - IConditionFactory.MakeAndOr
---

# IConditionFactory::MakeAndOr


## -description

Creates a condition node that is a logical conjunction (AND) or disjunction (OR) of a collection of subconditions.

## -parameters

### -param ct [in]

Type: <b><a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a></b>

The <a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a> of the condition node. The <b>CONDITION_TYPE</b> must be either <b>CT_AND_CONDITION</b> or <b>CT_OR_CONDITION</b>.

### -param peuSubs [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a>*</b>

A pointer to an enumeration of <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> objects, or <b>NULL</b> for an empty enumeration.

### -param fSimplify [in]

Type: <b>BOOL</b>

<b>TRUE</b> to logically simplify the result, if possible; then the result will not necessarily to be of the specified kind. <b>FALSE</b> if the result should have exactly the prescribed structure. 


An application that plans to execute a query based on the condition tree would typically benefit from setting this parameter to <b>TRUE</b>.

### -param ppcResult [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Receives the address of a pointer to the new <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> node.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There are no special condition trees for <b>TRUE</b> and <b>FALSE</b>. However, a condition tree consisting of an AND node with no subconditions is always <b>TRUE</b>, and a condition tree consisting of an OR node with no subconditions is always <b>FALSE</b>.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>