---
UID: NN:structuredquery.IQueryParser
title: IQueryParser (structuredquery.h)
description: Provides methods to parse an input string into an IQuerySolution object.
helpviewer_keywords: ["IQueryParser","IQueryParser interface [search]","IQueryParser interface [search]","described","_search_IQueryParser","search._search_IQueryParser","structuredquery/IQueryParser"]
old-location: search\_search_IQueryParser.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\iqueryparser.htm
ms.date: 12/05/2018
ms.keywords: IQueryParser, IQueryParser interface [search], IQueryParser interface [search],described, _search_IQueryParser, search._search_IQueryParser, structuredquery/IQueryParser
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
 - IQueryParser
 - structuredquery/IQueryParser
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
 - IQueryParser
---

# IQueryParser interface


## -description

Provides methods to parse an input string into an <a href="/windows/desktop/api/structuredquery/nn-structuredquery-iquerysolution">IQuerySolution</a> object.

## -inheritance

The <b>IQueryParser</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQueryParser</b> also has these types of members:

## -remarks

The <a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample">StructuredQuerySample</a> demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.

## -see-also

<a href="/windows/desktop/lwef/-search-2x-wds-aqsreference">Advanced Query Syntax</a>
