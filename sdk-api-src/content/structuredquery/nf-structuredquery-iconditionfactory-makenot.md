---
UID: NF:structuredquery.IConditionFactory.MakeNot
title: IConditionFactory::MakeNot (structuredquery.h)
description: Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node). (IConditionFactory.MakeNot)
helpviewer_keywords: ["IConditionFactory interface [search]","MakeNot method","IConditionFactory.MakeNot","IConditionFactory::MakeNot","MakeNot","MakeNot method [search]","MakeNot method [search]","IConditionFactory interface","_search_IConditionFactory_MakeNot","search._search_IConditionFactory_MakeNot","structuredquery/IConditionFactory::MakeNot"]
old-location: search\_search_IConditionFactory_MakeNot.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iconditionfactory\makenot.htm
ms.date: 12/05/2018
ms.keywords: IConditionFactory interface [search],MakeNot method, IConditionFactory.MakeNot, IConditionFactory::MakeNot, MakeNot, MakeNot method [search], MakeNot method [search],IConditionFactory interface, _search_IConditionFactory_MakeNot, search._search_IConditionFactory_MakeNot, structuredquery/IConditionFactory::MakeNot
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
 - IConditionFactory::MakeNot
 - structuredquery/IConditionFactory::MakeNot
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
 - IConditionFactory.MakeNot
---

# IConditionFactory::MakeNot


## -description

Creates a condition node that is a logical negation (NOT) of another condition (a subnode of this node).

## -parameters

### -param pcSub [in]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>*</b>

Pointer to the <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> subnode to be negated.

### -param fSimplify [in]

Type: <b>BOOL</b>

<b>TRUE</b> to logically simplify the result if possible; <b>FALSE</b> otherwise. In a query builder scenario, <i>fSimplify</i> should typically be set to VARIANT_FALSE.

### -param ppcResult [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Receives a pointer to the new <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> node.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Logically simplifying a condition node usually results in a smaller, more easily traversed and processed condition tree. For example, if <i>pcSub</i> is itself a negation condition with a subcondition C, then the double negation is logically resolved, and <i>ppcResult</i> is set to C. Without simplification, the resulting tree would look like NOT — NOT — C.
                

Applications that need to execute queries based on the condition tree would typically benefit from setting this parameter to <b>TRUE</b>.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory">IConditionFactory</a>



<a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditionfactory2">IConditionFactory2</a>



<b>Reference</b>
