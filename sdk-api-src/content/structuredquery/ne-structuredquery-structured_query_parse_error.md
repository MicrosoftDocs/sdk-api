---
UID: NE:structuredquery.tagSTRUCTURED_QUERY_PARSE_ERROR
title: STRUCTURED_QUERY_PARSE_ERROR (structuredquery.h)
description: A set of flags to be used with IQuerySolution::GetErrors to identify parsing error(s). Each parsing error indicates that one or more tokens were ignored when parsing a query string.
helpviewer_keywords: ["SQPE_EXTRA_CLOSING_PARENTHESIS","SQPE_EXTRA_OPENING_PARENTHESIS","SQPE_IGNORED_CONNECTOR","SQPE_IGNORED_KEYWORD","SQPE_IGNORED_MODIFIER","SQPE_NONE","SQPE_UNHANDLED","STRUCTURED_QUERY_PARSE_ERROR","STRUCTURED_QUERY_PARSE_ERROR enumeration [search]","_search_STRUCTURED_QUERY_PARSE_ERROR","search._search_STRUCTURED_QUERY_PARSE_ERROR","structuredquery/SQPE_EXTRA_CLOSING_PARENTHESIS","structuredquery/SQPE_EXTRA_OPENING_PARENTHESIS","structuredquery/SQPE_IGNORED_CONNECTOR","structuredquery/SQPE_IGNORED_KEYWORD","structuredquery/SQPE_IGNORED_MODIFIER","structuredquery/SQPE_NONE","structuredquery/SQPE_UNHANDLED","structuredquery/STRUCTURED_QUERY_PARSE_ERROR"]
old-location: search\_search_STRUCTURED_QUERY_PARSE_ERROR.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\structured_query_parse_error.htm
ms.date: 12/05/2018
ms.keywords: SQPE_EXTRA_CLOSING_PARENTHESIS, SQPE_EXTRA_OPENING_PARENTHESIS, SQPE_IGNORED_CONNECTOR, SQPE_IGNORED_KEYWORD, SQPE_IGNORED_MODIFIER, SQPE_NONE, SQPE_UNHANDLED, STRUCTURED_QUERY_PARSE_ERROR, STRUCTURED_QUERY_PARSE_ERROR enumeration [search], _search_STRUCTURED_QUERY_PARSE_ERROR, search._search_STRUCTURED_QUERY_PARSE_ERROR, structuredquery/SQPE_EXTRA_CLOSING_PARENTHESIS, structuredquery/SQPE_EXTRA_OPENING_PARENTHESIS, structuredquery/SQPE_IGNORED_CONNECTOR, structuredquery/SQPE_IGNORED_KEYWORD, structuredquery/SQPE_IGNORED_MODIFIER, structuredquery/SQPE_NONE, structuredquery/SQPE_UNHANDLED, structuredquery/STRUCTURED_QUERY_PARSE_ERROR
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: STRUCTURED_QUERY_PARSE_ERROR
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - tagSTRUCTURED_QUERY_PARSE_ERROR
 - structuredquery/tagSTRUCTURED_QUERY_PARSE_ERROR
 - STRUCTURED_QUERY_PARSE_ERROR
 - structuredquery/STRUCTURED_QUERY_PARSE_ERROR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Structuredquery.h
api_name:
 - STRUCTURED_QUERY_PARSE_ERROR
---

# STRUCTURED_QUERY_PARSE_ERROR enumeration


## -description

A set of flags to be used with <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iquerysolution-geterrors">IQuerySolution::GetErrors</a> to identify parsing error(s). Each parsing error indicates that one or more tokens were ignored when parsing a query string.

## -enum-fields

### -field SQPE_NONE:0

No error.

### -field SQPE_EXTRA_OPENING_PARENTHESIS

An extraneous <b>(</b>.

### -field SQPE_EXTRA_CLOSING_PARENTHESIS

An extraneous <b>)</b>.

### -field SQPE_IGNORED_MODIFIER

An extraneous <b>NOT</b>, <b>&lt;</b>, <b>&gt;</b>, <b>=</b>, and so forth.

### -field SQPE_IGNORED_CONNECTOR

An extraneous <b>AND</b> or <b>OR</b>.

### -field SQPE_IGNORED_KEYWORD

A property or other keyword used in the wrong context.

### -field SQPE_UNHANDLED

Any other parse error.

## -see-also

<a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-irichchunk">IRichChunk</a>
