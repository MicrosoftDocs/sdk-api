---
UID: NE:structuredquery.tagSTRUCTURED_QUERY_PARSE_ERROR
title: tagSTRUCTURED_QUERY_PARSE_ERROR
author: windows-driver-content
description: A set of flags to be used with IQuerySolution::GetErrors to indentify parsing error(s). Each parsing error indicates that one or more tokens were ignored when parsing a query string.
old-location: search\_search_STRUCTURED_QUERY_PARSE_ERROR.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\structured_query_parse_error.htm
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SQPE_EXTRA_CLOSING_PARENTHESIS, SQPE_EXTRA_OPENING_PARENTHESIS, SQPE_IGNORED_CONNECTOR, SQPE_IGNORED_KEYWORD, SQPE_IGNORED_MODIFIER, SQPE_NONE, SQPE_UNHANDLED, STRUCTURED_QUERY_PARSE_ERROR, STRUCTURED_QUERY_PARSE_ERROR enumeration [search], _search_STRUCTURED_QUERY_PARSE_ERROR, search._search_STRUCTURED_QUERY_PARSE_ERROR, structuredquery/SQPE_EXTRA_CLOSING_PARENTHESIS, structuredquery/SQPE_EXTRA_OPENING_PARENTHESIS, structuredquery/SQPE_IGNORED_CONNECTOR, structuredquery/SQPE_IGNORED_KEYWORD, structuredquery/SQPE_IGNORED_MODIFIER, structuredquery/SQPE_NONE, structuredquery/SQPE_UNHANDLED, structuredquery/STRUCTURED_QUERY_PARSE_ERROR, tagSTRUCTURED_QUERY_PARSE_ERROR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnalignedStringCchLengthW (Unicode) and StringCchLengthA (ANSI)
req.idl: Structuredquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: STRUCTURED_QUERY_PARSE_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Structuredquery.h
api_name:
-	STRUCTURED_QUERY_PARSE_ERROR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# tagSTRUCTURED_QUERY_PARSE_ERROR enumeration


## -description


A set of flags to be used with <a href="https://msdn.microsoft.com/50eead1a-5eb9-4bc9-ba54-c6dc77284f4d">IQuerySolution::GetErrors</a> to indentify parsing error(s). Each parsing error indicates that one or more tokens were ignored when parsing a query string.


## -enum-fields




### -field SQPE_NONE

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




<a href="https://msdn.microsoft.com/5fcc5c82-8d56-4495-8248-cf2fd19dd85a">IRichChunk</a>
 

 

