---
UID: NF:structuredquery.IQueryParser.GetSchemaProvider
title: IQueryParser::GetSchemaProvider (structuredquery.h)
description: Retrieves a schema provider for browsing the currently loaded schema.
helpviewer_keywords: ["GetSchemaProvider","GetSchemaProvider method [search]","GetSchemaProvider method [search]","IQueryParser interface","IQueryParser interface [search]","GetSchemaProvider method","IQueryParser.GetSchemaProvider","IQueryParser::GetSchemaProvider","_search_IQueryParser_GetSchemaProvider","search._search_IQueryParser_GetSchemaProvider","structuredquery/IQueryParser::GetSchemaProvider"]
old-location: search\_search_IQueryParser_GetSchemaProvider.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\getschemaprovider.htm
ms.date: 12/05/2018
ms.keywords: GetSchemaProvider, GetSchemaProvider method [search], GetSchemaProvider method [search],IQueryParser interface, IQueryParser interface [search],GetSchemaProvider method, IQueryParser.GetSchemaProvider, IQueryParser::GetSchemaProvider, _search_IQueryParser_GetSchemaProvider, search._search_IQueryParser_GetSchemaProvider, structuredquery/IQueryParser::GetSchemaProvider
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
 - IQueryParser::GetSchemaProvider
 - structuredquery/IQueryParser::GetSchemaProvider
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
 - IQueryParser.GetSchemaProvider
---

# IQueryParser::GetSchemaProvider


## -description

Retrieves a schema provider for browsing the currently loaded schema.

## -parameters

### -param ppSchemaProvider [out, retval]

Type: <b><a href="/windows/desktop/api/structuredquery/nn-structuredquery-ischemaprovider">ISchemaProvider</a>**</b>

Receives the address of a pointer to an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-ischemaprovider">ISchemaProvider</a> object. The calling application must release it by invoking its <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.