---
UID: NF:structuredquery.ISchemaProvider.MetaData
title: ISchemaProvider::MetaData (structuredquery.h)
description: Retrieves an enumeration of global IMetaData objects for the loaded schema.
helpviewer_keywords: ["ISchemaProvider interface [search]","MetaData method","ISchemaProvider.MetaData","ISchemaProvider::MetaData","MetaData","MetaData method [search]","MetaData method [search]","ISchemaProvider interface","_search_ISchemaProvider_MetaData","search._search_ISchemaProvider_MetaData","structuredquery/ISchemaProvider::MetaData"]
old-location: search\_search_ISchemaProvider_MetaData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\metadata.htm
ms.date: 12/05/2018
ms.keywords: ISchemaProvider interface [search],MetaData method, ISchemaProvider.MetaData, ISchemaProvider::MetaData, MetaData, MetaData method [search], MetaData method [search],ISchemaProvider interface, _search_ISchemaProvider_MetaData, search._search_ISchemaProvider_MetaData, structuredquery/ISchemaProvider::MetaData
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
 - ISchemaProvider::MetaData
 - structuredquery/ISchemaProvider::MetaData
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
 - ISchemaProvider.MetaData
---

# ISchemaProvider::MetaData


## -description

Retrieves an enumeration of global <a href="/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects for the loaded schema.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The desired IID of the result, either IID_IEnumUnknown or IID_IEnumVARIANT.

### -param pMetaData [out, retval]

Type: <b>void**</b>

Receives a pointer to an enumeration of the <a href="/windows/desktop/api/structuredquery/nn-structuredquery-imetadata">IMetaData</a> objects. The calling application must release it by calling its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.