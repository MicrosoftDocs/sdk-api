---
UID: NF:structuredquery.IEntity.MetaData
title: IEntity::MetaData (structuredquery.h)
description: Retrieves an enumeration of IMetaData objects for this entity.
helpviewer_keywords: ["IEntity interface [search]","MetaData method","IEntity.MetaData","IEntity::MetaData","MetaData","MetaData method [search]","MetaData method [search]","IEntity interface","_search_IEntity_MetaData","search._search_IEntity_MetaData","structuredquery/IEntity::MetaData"]
old-location: search\_search_IEntity_MetaData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ientity\metadata.htm
ms.date: 12/05/2018
ms.keywords: IEntity interface [search],MetaData method, IEntity.MetaData, IEntity::MetaData, MetaData, MetaData method [search], MetaData method [search],IEntity interface, _search_IEntity_MetaData, search._search_IEntity_MetaData, structuredquery/IEntity::MetaData
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
 - IEntity::MetaData
 - structuredquery/IEntity::MetaData
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
 - IEntity.MetaData
---

# IEntity::MetaData


## -description

Retrieves an enumeration of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects for this entity.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.

### -param pMetaData [out, retval]

Type: <b>void**</b>

Receives the address of a pointer to an enumeration of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.