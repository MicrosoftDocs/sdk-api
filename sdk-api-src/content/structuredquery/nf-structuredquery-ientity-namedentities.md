---
UID: NF:structuredquery.IEntity.NamedEntities
title: IEntity::NamedEntities (structuredquery.h)
description: Retrieves an enumeration of INamedEntity objects, one for each known named entity of this type.
helpviewer_keywords: ["IEntity interface [search]","NamedEntities method","IEntity.NamedEntities","IEntity::NamedEntities","NamedEntities","NamedEntities method [search]","NamedEntities method [search]","IEntity interface","_search_IEntity_NamedEntities","search._search_IEntity_NamedEntities","structuredquery/IEntity::NamedEntities"]
old-location: search\_search_IEntity_NamedEntities.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\namedentities.htm
ms.date: 12/05/2018
ms.keywords: IEntity interface [search],NamedEntities method, IEntity.NamedEntities, IEntity::NamedEntities, NamedEntities, NamedEntities method [search], NamedEntities method [search],IEntity interface, _search_IEntity_NamedEntities, search._search_IEntity_NamedEntities, structuredquery/IEntity::NamedEntities
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
 - IEntity::NamedEntities
 - structuredquery/IEntity::NamedEntities
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
 - IEntity.NamedEntities
---

# IEntity::NamedEntities


## -description

Retrieves an enumeration of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> objects, one for each known named entity of this type.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.

### -param pNamedEntities [out, retval]

Type: <b>void**</b>

Receives the address of a pointer to an enumeration of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> objects, one for each known named entity of this type.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.