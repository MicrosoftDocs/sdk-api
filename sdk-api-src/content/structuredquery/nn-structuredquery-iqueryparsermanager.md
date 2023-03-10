---
UID: NN:structuredquery.IQueryParserManager
title: IQueryParserManager (structuredquery.h)
description: Provides methods to create, initialize, and change options for an IQueryParser object.
helpviewer_keywords: ["IQueryParserManager","IQueryParserManager interface [search]","IQueryParserManager interface [search]","described","_search_IQueryParserManager","search._search_IQueryParserManager","structuredquery/IQueryParserManager"]
old-location: search\_search_IQueryParserManager.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparsermanager\iqueryparsermanager.htm
ms.date: 12/05/2018
ms.keywords: IQueryParserManager, IQueryParserManager interface [search], IQueryParserManager interface [search],described, _search_IQueryParserManager, search._search_IQueryParserManager, structuredquery/IQueryParserManager
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
 - IQueryParserManager
 - structuredquery/IQueryParserManager
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
 - IQueryParserManager
---

# IQueryParserManager interface


## -description

Provides methods to create, initialize, and change options for an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iqueryparser">IQueryParser</a> object.

## -inheritance

The <b>IQueryParserManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryParserManager</b> also has these types of members:

## -remarks

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="/windows/desktop/lwef/-search-2x-wds-aqsreference">Advanced Query Syntax</a>
