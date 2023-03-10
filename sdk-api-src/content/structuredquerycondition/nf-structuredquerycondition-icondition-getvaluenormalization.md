---
UID: NF:structuredquerycondition.ICondition.GetValueNormalization
title: ICondition::GetValueNormalization (structuredquerycondition.h)
description: Retrieves the character-normalized value of the search condition node.
helpviewer_keywords: ["GetValueNormalization","GetValueNormalization method [search]","GetValueNormalization method [search]","ICondition interface","ICondition interface [search]","GetValueNormalization method","ICondition.GetValueNormalization","ICondition::GetValueNormalization","_search_ICondition_GetValueNormalization","search._search_ICondition_GetValueNormalization","structuredquerycondition/ICondition::GetValueNormalization"]
old-location: search\_search_ICondition_GetValueNormalization.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getvaluenormalization.htm
ms.date: 12/05/2018
ms.keywords: GetValueNormalization, GetValueNormalization method [search], GetValueNormalization method [search],ICondition interface, ICondition interface [search],GetValueNormalization method, ICondition.GetValueNormalization, ICondition::GetValueNormalization, _search_ICondition_GetValueNormalization, search._search_ICondition_GetValueNormalization, structuredquerycondition/ICondition::GetValueNormalization
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
 - ICondition::GetValueNormalization
 - structuredquerycondition/ICondition::GetValueNormalization
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
 - ICondition.GetValueNormalization
---

# ICondition::GetValueNormalization


## -description

Retrieves the character-normalized value of the search condition node.

## -parameters

### -param ppszNormalization [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a Unicode string representation of the value.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.

## -remarks

In <b>Windows 7 and later</b>, if the value of the leaf node is <b>VT_EMPTY</b>, <i>ppwszNormalization</i> points to an empty string. If the value is a string, such as VT_LPWSTR, VT_BSTR or VT_LPSTR, then <i>ppwszNormalization</i> is set to a character-normalized form of the value. In other cases, <i>ppwszNormalization</i> is set to some other character-normalized string representation of the value.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>