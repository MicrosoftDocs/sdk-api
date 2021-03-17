---
UID: NF:structuredquerycondition.ICondition.GetValueType
title: ICondition::GetValueType (structuredquerycondition.h)
description: Retrieves the semantic type of the value of the search condition node.
helpviewer_keywords: ["GetValueType","GetValueType method [search]","GetValueType method [search]","ICondition interface","ICondition interface [search]","GetValueType method","ICondition.GetValueType","ICondition::GetValueType","_search_ICondition_GetValueType","search._search_ICondition_GetValueType","structuredquerycondition/ICondition::GetValueType"]
old-location: search\_search_ICondition_GetValueType.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getvaluetype.htm
ms.date: 12/05/2018
ms.keywords: GetValueType, GetValueType method [search], GetValueType method [search],ICondition interface, ICondition interface [search],GetValueType method, ICondition.GetValueType, ICondition::GetValueType, _search_ICondition_GetValueType, search._search_ICondition_GetValueType, structuredquerycondition/ICondition::GetValueType
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
 - ICondition::GetValueType
 - structuredquerycondition/ICondition::GetValueType
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
 - ICondition.GetValueType
---

# ICondition::GetValueType


## -description

Retrieves the semantic type of the value of the search condition node.

## -parameters

### -param ppszValueTypeName [out, retval]

Type: <b>LPWSTR*</b>

Receives either a pointer to the semantic type of the value as a Unicode string or <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>