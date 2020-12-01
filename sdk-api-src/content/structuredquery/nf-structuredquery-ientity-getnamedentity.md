---
UID: NF:structuredquery.IEntity.GetNamedEntity
title: IEntity::GetNamedEntity (structuredquery.h)
description: Retrieves an INamedEntity object based on an entity name.
helpviewer_keywords: ["GetNamedEntity","GetNamedEntity method [search]","GetNamedEntity method [search]","IEntity interface","IEntity interface [search]","GetNamedEntity method","IEntity.GetNamedEntity","IEntity::GetNamedEntity","_search_IEntity_GetNamedEntity","search._search_IEntity_GetNamedEntity","structuredquery/IEntity::GetNamedEntity"]
old-location: search\_search_IEntity_GetNamedEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\getnamedentity.htm
ms.date: 12/05/2018
ms.keywords: GetNamedEntity, GetNamedEntity method [search], GetNamedEntity method [search],IEntity interface, IEntity interface [search],GetNamedEntity method, IEntity.GetNamedEntity, IEntity::GetNamedEntity, _search_IEntity_GetNamedEntity, search._search_IEntity_GetNamedEntity, structuredquery/IEntity::GetNamedEntity
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
 - IEntity::GetNamedEntity
 - structuredquery/IEntity::GetNamedEntity
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
 - IEntity.GetNamedEntity
---

# IEntity::GetNamedEntity


## -description

Retrieves an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> object based on an entity name.

## -parameters

### -param pszValue [in]

Type: <b>LPCWSTR</b>

The name of an entity to be found.

### -param ppNamedEntity [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a>**</b>

Receives a pointer to the <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> object that was named in <i>pszValue</i>. <b>NULL</b> if no named entity was found.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or S_False if the named entity cannot be found.