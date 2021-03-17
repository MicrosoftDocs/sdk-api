---
UID: NF:structuredquery.ISchemaProvider.LookupAuthoredNamedEntity
title: ISchemaProvider::LookupAuthoredNamedEntity (structuredquery.h)
description: Finds named entities of a specified type in a tokenized string, and returns the value of the entity and the number of tokens the entity value occupies.
helpviewer_keywords: ["ISchemaProvider interface [search]","LookupAuthoredNamedEntity method","ISchemaProvider.LookupAuthoredNamedEntity","ISchemaProvider::LookupAuthoredNamedEntity","LookupAuthoredNamedEntity","LookupAuthoredNamedEntity method [search]","LookupAuthoredNamedEntity method [search]","ISchemaProvider interface","_search_ISchemaProvider_LookupAuthoredNamedEntity","search._search_ISchemaProvider_LookupAuthoredNamedEntity","structuredquery/ISchemaProvider::LookupAuthoredNamedEntity"]
old-location: search\_search_ISchemaProvider_LookupAuthoredNamedEntity.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\lookupauthorednamedentity.htm
ms.date: 12/05/2018
ms.keywords: ISchemaProvider interface [search],LookupAuthoredNamedEntity method, ISchemaProvider.LookupAuthoredNamedEntity, ISchemaProvider::LookupAuthoredNamedEntity, LookupAuthoredNamedEntity, LookupAuthoredNamedEntity method [search], LookupAuthoredNamedEntity method [search],ISchemaProvider interface, _search_ISchemaProvider_LookupAuthoredNamedEntity, search._search_ISchemaProvider_LookupAuthoredNamedEntity, structuredquery/ISchemaProvider::LookupAuthoredNamedEntity
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
 - ISchemaProvider::LookupAuthoredNamedEntity
 - structuredquery/ISchemaProvider::LookupAuthoredNamedEntity
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
 - ISchemaProvider.LookupAuthoredNamedEntity
---

# ISchemaProvider::LookupAuthoredNamedEntity


## -description

Finds named entities of a specified type in a tokenized string, and returns the value of the entity and the number of tokens the entity value occupies.

## -parameters

### -param pEntity [in]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a>*</b>

A pointer to an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ientity">IEntity</a> object identifying the type of named entity to locate.

### -param pszInputString [in]

Type: <b>LPCWSTR</b>

An input string in which to search for named entity keywords.

### -param pTokenCollection [in]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-itokencollection">ITokenCollection</a>*</b>

A pointer to the tokenization of the string in the <i>pszInputString</i> parameter.

### -param cTokensBegin [in]

Type: <b>ULONG</b>

The zero-based position of a token in the <i>pTokenCollection</i> from which to start searching.

### -param pcTokensLength [out]

Type: <b>ULONG*</b>

Receives a pointer to the number of tokens covered by the named entity keyword that was found.

### -param ppszValue [out]

Type: <b>LPWSTR*</b>

Receives a pointer to the value of the named entity that was found, as a Unicode string. The caller must free the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. An <a href="/windows/desktop/api/structuredquery/nn-structuredquery-inamedentity">INamedEntity</a> object can be obtained by calling the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-ientity-getnamedentity">GetNamedEntity</a> method of <i>pEntity</i> and passing the string that was received in this parameter.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the token sequence beginning at position <i>cTokensBegin</i> denotes a named entity of the specified (entity) type. If there is no such token sequence, returns S_FALSE.

## -remarks

The method finds only named entities authored with keywords in the schema, not named entities recognized by an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iconditiongenerator">IConditionGenerator</a> object.