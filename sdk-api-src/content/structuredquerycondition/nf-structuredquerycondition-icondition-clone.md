---
UID: NF:structuredquerycondition.ICondition.Clone
title: ICondition::Clone (structuredquerycondition.h)
description: Creates a deep copy of this ICondition object.
helpviewer_keywords: ["Clone","Clone method [search]","Clone method [search]","ICondition interface","ICondition interface [search]","Clone method","ICondition.Clone","ICondition::Clone","_search_ICondition_Clone","search._search_ICondition_Clone","structuredquerycondition/ICondition::Clone"]
old-location: search\_search_ICondition_Clone.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\clone.htm
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [search], Clone method [search],ICondition interface, ICondition interface [search],Clone method, ICondition.Clone, ICondition::Clone, _search_ICondition_Clone, search._search_ICondition_Clone, structuredquerycondition/ICondition::Clone
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
 - ICondition::Clone
 - structuredquerycondition/ICondition::Clone
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
 - ICondition.Clone
---

# ICondition::Clone


## -description

Creates a deep copy of this <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> object.

## -parameters

### -param ppc [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>**</b>

Receives a pointer to the clone of this <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Because there are no methods for modifying an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>, there are few occasions when this method is necessary. In many cases it is adequate to call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method on the <b>ICondition</b> to obtain an additional reference to the same object.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>