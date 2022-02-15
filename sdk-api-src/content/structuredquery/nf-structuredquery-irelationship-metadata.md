---
UID: NF:structuredquery.IRelationship.MetaData
title: IRelationship::MetaData (structuredquery.h)
description: Retrieves an enumeration of IMetaData objects for this relationship.
helpviewer_keywords: ["IRelationship interface [search]","MetaData method","IRelationship.MetaData","IRelationship::MetaData","MetaData","MetaData method [search]","MetaData method [search]","IRelationship interface","_search_IRelationship_MetaData","search._search_IRelationship_MetaData","structuredquery/IRelationship::MetaData"]
old-location: search\_search_IRelationship_MetaData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\irelationship\metadata.htm
ms.date: 12/05/2018
ms.keywords: IRelationship interface [search],MetaData method, IRelationship.MetaData, IRelationship::MetaData, MetaData, MetaData method [search], MetaData method [search],IRelationship interface, _search_IRelationship_MetaData, search._search_IRelationship_MetaData, structuredquery/IRelationship::MetaData
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
 - IRelationship::MetaData
 - structuredquery/IRelationship::MetaData
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
 - IRelationship.MetaData
---

# IRelationship::MetaData


## -description

Retrieves an enumeration of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects for this relationship.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.

### -param pMetaData [out, retval]

Type: <b>void**</b>

Receives a pointer to the enumeration of <a href="/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects. There may be multiple pairs with the same key (or the same value).

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.