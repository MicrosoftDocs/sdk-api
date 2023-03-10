---
UID: NF:structuredquerycondition.ICondition2.GetLocale
title: ICondition2::GetLocale (structuredquerycondition.h)
description: Retrieves the property name, operation, and value from a leaf search condition node. (ICondition2.GetLocale)
helpviewer_keywords: ["GetLocale","GetLocale method [search]","GetLocale method [search]","ICondition2 interface","ICondition2 interface [search]","GetLocale method","ICondition2.GetLocale","ICondition2::GetLocale","_search_ICondition2_GetLocale","search._search_ICondition2_GetLocale","structuredquerycondition/ICondition2::GetLocale"]
old-location: search\_search_ICondition2_GetLocale.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\ifaces\querying\icondition2\getlocale.htm
ms.date: 12/05/2018
ms.keywords: GetLocale, GetLocale method [search], GetLocale method [search],ICondition2 interface, ICondition2 interface [search],GetLocale method, ICondition2.GetLocale, ICondition2::GetLocale, _search_ICondition2_GetLocale, search._search_ICondition2_GetLocale, structuredquerycondition/ICondition2::GetLocale
req.header: structuredquerycondition.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Structuredquerycondition.idl
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
 - ICondition2::GetLocale
 - structuredquerycondition/ICondition2::GetLocale
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Structuredquerycondition.h
api_name:
 - ICondition2.GetLocale
---

# ICondition2::GetLocale


## -description

Retrieves the property name, operation, and value from a leaf search condition node.

## -parameters

### -param ppszLocaleName [out, optional]

Type: <b>LPWSTR*</b>

Receives the name of the locale of the leaf condition as a Unicode string. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, E_FAIL if this is not a leaf node, or an error value otherwise.

## -see-also

<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_operation">CONDITION_OPERATION</a>



<a href="/windows/win32/api/structuredquerycondition/ne-structuredquerycondition-condition_type">CONDITION_TYPE</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>



<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition2">ICondition2</a>



<b>Reference</b>
