---
UID: NF:structuredquery.ISchemaProvider.SaveBinary
title: ISchemaProvider::SaveBinary (structuredquery.h)
description: Saves the loaded schema as a schema binary at a specified path.
helpviewer_keywords: ["ISchemaProvider interface [search]","SaveBinary method","ISchemaProvider.SaveBinary","ISchemaProvider::SaveBinary","SaveBinary","SaveBinary method [search]","SaveBinary method [search]","ISchemaProvider interface","_search_ISchemaProvider_SaveBinary","search._search_ISchemaProvider_SaveBinary","structuredquery/ISchemaProvider::SaveBinary"]
old-location: search\_search_ISchemaProvider_SaveBinary.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\savebinary.htm
ms.date: 12/05/2018
ms.keywords: ISchemaProvider interface [search],SaveBinary method, ISchemaProvider.SaveBinary, ISchemaProvider::SaveBinary, SaveBinary, SaveBinary method [search], SaveBinary method [search],ISchemaProvider interface, _search_ISchemaProvider_SaveBinary, search._search_ISchemaProvider_SaveBinary, structuredquery/ISchemaProvider::SaveBinary
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
 - ISchemaProvider::SaveBinary
 - structuredquery/ISchemaProvider::SaveBinary
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
 - ISchemaProvider.SaveBinary
---

# ISchemaProvider::SaveBinary


## -description

Saves the loaded schema as a schema binary at a specified path.

## -parameters

### -param pszSchemaBinaryPath [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated Unicode string that contains the fully qualified path at which to save the schema binary.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any existing file at the location specified by <i>pszSchemaBinaryPath</i> is overwritten.

