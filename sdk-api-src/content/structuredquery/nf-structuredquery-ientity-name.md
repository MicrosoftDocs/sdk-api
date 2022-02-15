---
UID: NF:structuredquery.IEntity.Name
title: IEntity::Name (structuredquery.h)
description: Retrieves the name of this entity.
helpviewer_keywords: ["IEntity interface [search]","Name method","IEntity.Name","IEntity::Name","Name","Name method [search]","Name method [search]","IEntity interface","_search_IEntity_Name","search._search_IEntity_Name","structuredquery/IEntity::Name"]
old-location: search\_search_IEntity_Name.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\name.htm
ms.date: 12/05/2018
ms.keywords: IEntity interface [search],Name method, IEntity.Name, IEntity::Name, Name, Name method [search], Name method [search],IEntity interface, _search_IEntity_Name, search._search_IEntity_Name, structuredquery/IEntity::Name
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
 - IEntity::Name
 - structuredquery/IEntity::Name
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
 - IEntity.Name
---

# IEntity::Name


## -description

Retrieves the name of this entity.

## -parameters

### -param ppszName [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to the name of this entity as a Unicode string. The calling application must free the returned string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each name must be unique.