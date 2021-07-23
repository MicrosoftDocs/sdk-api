---
UID: NF:structuredquery.IRelationship.DefaultPhrase
title: IRelationship::DefaultPhrase (structuredquery.h)
description: Retrieves the default phrase to use for this relationship in restatements.
helpviewer_keywords: ["DefaultPhrase","DefaultPhrase method [search]","DefaultPhrase method [search]","IRelationship interface","IRelationship interface [search]","DefaultPhrase method","IRelationship.DefaultPhrase","IRelationship::DefaultPhrase","_search_IRelationship_DefaultPhrase","search._search_IRelationship_DefaultPhrase","structuredquery/IRelationship::DefaultPhrase"]
old-location: search\_search_IRelationship_DefaultPhrase.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\defaultphrase.htm
ms.date: 12/05/2018
ms.keywords: DefaultPhrase, DefaultPhrase method [search], DefaultPhrase method [search],IRelationship interface, IRelationship interface [search],DefaultPhrase method, IRelationship.DefaultPhrase, IRelationship::DefaultPhrase, _search_IRelationship_DefaultPhrase, search._search_IRelationship_DefaultPhrase, structuredquery/IRelationship::DefaultPhrase
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
 - IRelationship::DefaultPhrase
 - structuredquery/IRelationship::DefaultPhrase
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
 - IRelationship.DefaultPhrase
---

# IRelationship::DefaultPhrase


## -description

Retrieves the default phrase to use for this relationship in restatements.

## -parameters

### -param ppszPhrase [out, retval]

Type: <b>LPWSTR*</b>

Receives the default phrase as a Unicode string. The calling application must free the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.