---
UID: NF:structuredquery.ISchemaProvider.Localize
title: ISchemaProvider::Localize (structuredquery.h)
description: Localizes the currently loaded schema for a specified locale.
helpviewer_keywords: ["ISchemaProvider interface [search]","Localize method","ISchemaProvider.Localize","ISchemaProvider::Localize","Localize","Localize method [search]","Localize method [search]","ISchemaProvider interface","_search_ISchemaProvider_Localize","search._search_ISchemaProvider_Localize","structuredquery/ISchemaProvider::Localize"]
old-location: search\_search_ISchemaProvider_Localize.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\ischemaprovider\localize.htm
ms.date: 12/05/2018
ms.keywords: ISchemaProvider interface [search],Localize method, ISchemaProvider.Localize, ISchemaProvider::Localize, Localize, Localize method [search], Localize method [search],ISchemaProvider interface, _search_ISchemaProvider_Localize, search._search_ISchemaProvider_Localize, structuredquery/ISchemaProvider::Localize
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
 - ISchemaProvider::Localize
 - structuredquery/ISchemaProvider::Localize
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
 - ISchemaProvider.Localize
---

# ISchemaProvider::Localize


## -description

Localizes the currently loaded schema for a specified locale.

## -parameters

### -param lcid [in]

Type: <b>LCID</b>

The locale to localize for.

### -param pSchemaLocalizerSupport [in]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ischemalocalizersupport">ISchemaLocalizerSupport</a>*</b>

Pointer to an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ischemalocalizersupport">ISchemaLocalizerSupport</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before this method is called, the loaded schema should typically be a schema that is not localized, such as the one in %SYSTEMROOT%\System32\StructuredQuerySchema.bin. This method makes the loaded schema suitable for parsing queries in the specified locale, using the object specified in the <i>pSchemaLocalizerSupport</i> parameter. The localized schema can then be saved into a schema binary by calling the <a href="/windows/desktop/api/structuredquery/nf-structuredquery-ischemaprovider-savebinary">ISchemaProvider::SaveBinary</a> method.

Most applications should use <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparsermanager-createloadedparser">CreateLoadedParser</a> to obtain a query parser loaded with a localized schema, instead of using this method explicitly.