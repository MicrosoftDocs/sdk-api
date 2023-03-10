---
UID: NF:structuredquery.INamedEntity.GetValue
title: INamedEntity::GetValue (structuredquery.h)
description: Retrieves the value of this named entity as a string.
helpviewer_keywords: ["GetValue","GetValue method [search]","GetValue method [search]","INamedEntity interface","INamedEntity interface [search]","GetValue method","INamedEntity.GetValue","INamedEntity::GetValue","_search_INamedEntity_GetValue","search._search_INamedEntity_GetValue","structuredquery/INamedEntity::GetValue"]
old-location: search\_search_INamedEntity_GetValue.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\inamedentity\getvalue.htm
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [search], GetValue method [search],INamedEntity interface, INamedEntity interface [search],GetValue method, INamedEntity.GetValue, INamedEntity::GetValue, _search_INamedEntity_GetValue, search._search_INamedEntity_GetValue, structuredquery/INamedEntity::GetValue
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INamedEntity::GetValue
 - structuredquery/INamedEntity::GetValue
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
 - INamedEntity.GetValue
---

# INamedEntity::GetValue


## -description

Retrieves the value of this named entity as a string.

## -parameters

### -param ppszValue [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the value of the named entity as a Unicode string. The calling application must free the returned string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.