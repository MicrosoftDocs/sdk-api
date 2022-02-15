---
UID: NF:structuredquery.IRelationship.Name
title: IRelationship::Name (structuredquery.h)
description: Retrieves the name of the relationship.
helpviewer_keywords: ["IRelationship interface [search]","Name method","IRelationship.Name","IRelationship::Name","Name","Name method [search]","Name method [search]","IRelationship interface","_search_IRelationship_Name","search._search_IRelationship_Name","structuredquery/IRelationship::Name"]
old-location: search\_search_IRelationship_Name.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\name.htm
ms.date: 12/05/2018
ms.keywords: IRelationship interface [search],Name method, IRelationship.Name, IRelationship::Name, Name, Name method [search], Name method [search],IRelationship interface, _search_IRelationship_Name, search._search_IRelationship_Name, structuredquery/IRelationship::Name
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
 - IRelationship::Name
 - structuredquery/IRelationship::Name
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
 - IRelationship.Name
---

# IRelationship::Name


## -description

Retrieves the name of the relationship.

## -parameters

### -param ppszName [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the name of the relationship as a Unicode string. The calling application must free the returned string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.