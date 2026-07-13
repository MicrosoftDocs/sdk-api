---
UID: NF:structuredquery.IQueryParser.SetMultiOption
title: IQueryParser::SetMultiOption (structuredquery.h)
description: Sets a complex option, such as a specified condition generator, to use when parsing an input string.
helpviewer_keywords: ["IQueryParser interface [search]","SetMultiOption method","IQueryParser.SetMultiOption","IQueryParser::SetMultiOption","SetMultiOption","SetMultiOption method [search]","SetMultiOption method [search]","IQueryParser interface","_search_IQueryParser_SetMultiOption","search._search_IQueryParser_SetMultiOption","structuredquery/IQueryParser::SetMultiOption"]
old-location: search\_search_IQueryParser_SetMultiOption.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\iqueryparser\setmultioption.htm
ms.date: 12/05/2018
ms.keywords: IQueryParser interface [search],SetMultiOption method, IQueryParser.SetMultiOption, IQueryParser::SetMultiOption, SetMultiOption, SetMultiOption method [search], SetMultiOption method [search],IQueryParser interface, _search_IQueryParser_SetMultiOption, search._search_IQueryParser_SetMultiOption, structuredquery/IQueryParser::SetMultiOption
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
 - IQueryParser::SetMultiOption
 - structuredquery/IQueryParser::SetMultiOption
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
 - IQueryParser.SetMultiOption
---

# IQueryParser::SetMultiOption


## -description

Sets a complex option, such as a specified condition generator, to use when parsing an input string.

## -parameters

### -param option [in]

Type: <b><a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_multioption">STRUCTURED_QUERY_MULTIOPTION</a></b>

The complex option to be set.

### -param pszOptionKey [in]

Type: <b>LPCWSTR</b>

A Unicode string that is interpreted differently for each value of the <i>option</i> parameter. For more information, see <a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_multioption">STRUCTURED_QUERY_MULTIOPTION</a>.

### -param pOptionValue [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Pointer to a <a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_multioption">PROPVARIANT</a> that is interpreted differently for each value of the <i>option</i> parameter. For more information, see <a href="/windows/desktop/api/structuredquery/ne-structuredquery-structured_query_multioption">STRUCTURED_QUERY_MULTIOPTION</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.