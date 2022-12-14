---
UID: NF:structuredquery.IMetaData.GetData
title: IMetaData::GetData (structuredquery.h)
description: Retrieves one key/value pair from the metadata of an IEntity, IRelationship, or ISchemaProvider object.
helpviewer_keywords: ["GetData","GetData method [search]","GetData method [search]","IMetaData interface","IMetaData interface [search]","GetData method","IMetaData.GetData","IMetaData::GetData","_search_IMetaData_GetData","search._search_IMetaData_GetData","structuredquery/IMetaData::GetData"]
old-location: search\_search_IMetaData_GetData.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\imetadata\getdata.htm
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [search], GetData method [search],IMetaData interface, IMetaData interface [search],GetData method, IMetaData.GetData, IMetaData::GetData, _search_IMetaData_GetData, search._search_IMetaData_GetData, structuredquery/IMetaData::GetData
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
 - IMetaData::GetData
 - structuredquery/IMetaData::GetData
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
 - IMetaData.GetData
---

# IMetaData::GetData


## -description

Retrieves one key/value pair from the metadata of an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>, <a href="/windows/desktop/api/structuredquery/nn-structuredquery-irelationship">IRelationship</a>, or <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ischemaprovider">ISchemaProvider</a> object.

## -parameters

### -param ppszKey [out]

Type: <b>LPCWSTR*</b>

Receives the key of the metadata pair as a Unicode string. The calling application must free the returned string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param ppszValue [out]

Type: <b>LPWSTR*</b>

Receives the value of the metadata pair as a Unicode string. The calling application must free the returned string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.