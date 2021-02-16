---
UID: NF:structuredquerycondition.ICondition.GetSubConditions
title: ICondition::GetSubConditions (structuredquerycondition.h)
description: Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection.
helpviewer_keywords: ["GetSubConditions","GetSubConditions method [search]","GetSubConditions method [search]","ICondition interface","ICondition interface [search]","GetSubConditions method","ICondition.GetSubConditions","ICondition::GetSubConditions","_search_ICondition_GetSubConditions","search._search_ICondition_GetSubConditions","structuredquerycondition/ICondition::GetSubConditions"]
old-location: search\_search_ICondition_GetSubConditions.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getsubconditions.htm
ms.date: 12/05/2018
ms.keywords: GetSubConditions, GetSubConditions method [search], GetSubConditions method [search],ICondition interface, ICondition interface [search],GetSubConditions method, ICondition.GetSubConditions, ICondition::GetSubConditions, _search_ICondition_GetSubConditions, search._search_ICondition_GetSubConditions, structuredquerycondition/ICondition::GetSubConditions
req.header: structuredquerycondition.h
req.include-header: Structuredquery.h
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
 - ICondition::GetSubConditions
 - structuredquerycondition/ICondition::GetSubConditions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - structuredquerycondition.h
api_name:
 - ICondition.GetSubConditions
---

# ICondition::GetSubConditions


## -description

Retrieves a collection of the subconditions of the search condition node and the IID of the interface for enumerating the collection.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the enumerating interface: either IID_IEnumUnknown, IID_IEnumVARIANT or (for a negation condition) IID_ICondition.

### -param ppv [out, retval]

Type: <b>void**</b>

Receives a collection of zero or more <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> objects. Each object is a subcondition of this condition node. If <i>riid</i> was IID_ICondition and this is a negation condition, this parameter receives the single subcondition.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is a leaf node, or an error value otherwise.

## -remarks

The <i>riid</i> parameter must be the <b>GUID</b> of an <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> or <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface or in the case of a negation node, IID_ICondition.

If the subcondition is a negation node, <i>ppv</i> is set to an enumeration of one element.

If the node is a conjunction or disjunction node, <i>ppv</i> is set to an enumeration of the subconditions.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>