---
UID: NF:structuredquery.ISchemaProvider.GetEntity
title: ISchemaProvider::GetEntity (structuredquery.h)
description: Retrieves an entity by name from the loaded schema.
helpviewer_keywords: ["GetEntity","GetEntity method [search]","GetEntity method [search]","ISchemaProvider interface","ISchemaProvider interface [search]","GetEntity method","ISchemaProvider.GetEntity","ISchemaProvider::GetEntity","_search_ISchemaProvider_GetEntity","search._search_ISchemaProvider_GetEntity","structuredquery/ISchemaProvider::GetEntity"]
old-location: search\_search_ISchemaProvider_GetEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\getentity.htm
ms.date: 12/05/2018
ms.keywords: GetEntity, GetEntity method [search], GetEntity method [search],ISchemaProvider interface, ISchemaProvider interface [search],GetEntity method, ISchemaProvider.GetEntity, ISchemaProvider::GetEntity, _search_ISchemaProvider_GetEntity, search._search_ISchemaProvider_GetEntity, structuredquery/ISchemaProvider::GetEntity
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
 - ISchemaProvider::GetEntity
 - structuredquery/ISchemaProvider::GetEntity
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
 - ISchemaProvider.GetEntity
---

# ISchemaProvider::GetEntity


## -description

Retrieves an entity by name from the loaded schema.

## -parameters

### -param pszEntityName [in]

Type: <b>LPCWSTR</b>

The name of the entity being requested.

### -param pEntity [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>**</b>

Receives the address of a pointer to the requested entity. The calling application must release the entity by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. If there is no entity with the specified name, this parameter is set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, S_FALSE if there is no entity with the specified name, or an error value otherwise.