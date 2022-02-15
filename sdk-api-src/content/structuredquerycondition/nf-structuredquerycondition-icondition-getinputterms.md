---
UID: NF:structuredquerycondition.ICondition.GetInputTerms
title: ICondition::GetInputTerms (structuredquerycondition.h)
description: For a leaf node, ICondition::GetInputTerms retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.
helpviewer_keywords: ["GetInputTerms","GetInputTerms method [search]","GetInputTerms method [search]","ICondition interface","ICondition interface [search]","GetInputTerms method","ICondition.GetInputTerms","ICondition::GetInputTerms","_search_ICondition_GetInputTerms","search._search_ICondition_GetInputTerms","structuredquerycondition/ICondition::GetInputTerms"]
old-location: search\_search_ICondition_GetInputTerms.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\icondition\getinputterms.htm
ms.date: 12/05/2018
ms.keywords: GetInputTerms, GetInputTerms method [search], GetInputTerms method [search],ICondition interface, ICondition interface [search],GetInputTerms method, ICondition.GetInputTerms, ICondition::GetInputTerms, _search_ICondition_GetInputTerms, search._search_ICondition_GetInputTerms, structuredquerycondition/ICondition::GetInputTerms
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
 - ICondition::GetInputTerms
 - structuredquerycondition/ICondition::GetInputTerms
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
 - ICondition.GetInputTerms
---

# ICondition::GetInputTerms


## -description

For a leaf node, <b>ICondition::GetInputTerms</b> retrieves information about what parts (or ranges) of the input string produced the property, the operation, and the value for the search condition node.

## -parameters

### -param ppPropertyTerm [out, optional]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> interface that provides information about what part of the input string produced the property of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.

### -param ppOperationTerm [out, optional]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> interface that provides information about what part of the input string produced the operation of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.

### -param ppValueTerm [out, optional]

Type: <b><a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> interface that provides information about what part of the input string produced the value of the leaf node, if that can be determined; otherwise, this parameter is set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any or all of the parameters <i>ppPropertyTerm</i>, <i>ppOperationTerm</i> and <i>ppValueTerm</i> can be <b>NULL</b>.

Each <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a> object retrieved by this method represents a range of tokens from the input string. The range tokens identifies the substring that produced the property, operation, or value of the input string. The <b>IRichChunk</b>'s <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> out parameter is not used.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>