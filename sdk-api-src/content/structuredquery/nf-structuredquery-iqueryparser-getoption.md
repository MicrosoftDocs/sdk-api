---
UID: NF:structuredquery.IQueryParser.GetOption
title: IQueryParser::GetOption (structuredquery.h)
description: Retrieves a specified simple option value for this query parser.
helpviewer_keywords: ["GetOption","GetOption method [search]","GetOption method [search]","IQueryParser interface","IQueryParser interface [search]","GetOption method","IQueryParser.GetOption","IQueryParser::GetOption","_search_IQueryParser_GetOption","search._search_IQueryParser_GetOption","structuredquery/IQueryParser::GetOption"]
old-location: search\_search_IQueryParser_GetOption.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\getoption.htm
ms.date: 12/05/2018
ms.keywords: GetOption, GetOption method [search], GetOption method [search],IQueryParser interface, IQueryParser interface [search],GetOption method, IQueryParser.GetOption, IQueryParser::GetOption, _search_IQueryParser_GetOption, search._search_IQueryParser_GetOption, structuredquery/IQueryParser::GetOption
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
 - IQueryParser::GetOption
 - structuredquery/IQueryParser::GetOption
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
 - IQueryParser.GetOption
---

# IQueryParser::GetOption


## -description

Retrieves a specified simple option value for this query parser.

## -parameters

### -param option [in]

Type: <b><a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_single_option">STRUCTURED_QUERY_SINGLE_OPTION</a></b>

The <a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_single_option">STRUCTURED_QUERY_SINGLE_OPTION</a> enumerated type that specifies the option to be retrieved.

### -param pOptionValue [out, retval]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Receives a pointer to the specified option value. For more information, see <a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_single_option">STRUCTURED_QUERY_SINGLE_OPTION</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.