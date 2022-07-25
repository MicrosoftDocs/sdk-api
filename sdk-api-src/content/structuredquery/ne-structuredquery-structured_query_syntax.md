---
UID: NE:structuredquery.tagSTRUCTURED_QUERY_SYNTAX
title: STRUCTURED_QUERY_SYNTAX (structuredquery.h)
description: Specifies the type of query syntax.
helpviewer_keywords: ["SQS_ADVANCED_QUERY_SYNTAX","SQS_NATURAL_QUERY_SYNTAX","SQS_NO_SYNTAX","STRUCTURED_QUERY_SYNTAX","STRUCTURED_QUERY_SYNTAX enumeration [search]","_search_STRUCTURED_QUERY_SYNTAX","search._search_STRUCTURED_QUERY_SYNTAX","structuredquery/SQS_ADVANCED_QUERY_SYNTAX","structuredquery/SQS_NATURAL_QUERY_SYNTAX","structuredquery/SQS_NO_SYNTAX","structuredquery/STRUCTURED_QUERY_SYNTAX"]
old-location: search\_search_STRUCTURED_QUERY_SYNTAX.htm
tech.root: search
ms.assetid: VS|SEARCH|~\search\wds3x\reference\enums\structured_query_syntax.htm
ms.date: 12/05/2018
ms.keywords: SQS_ADVANCED_QUERY_SYNTAX, SQS_NATURAL_QUERY_SYNTAX, SQS_NO_SYNTAX, STRUCTURED_QUERY_SYNTAX, STRUCTURED_QUERY_SYNTAX enumeration [search], _search_STRUCTURED_QUERY_SYNTAX, search._search_STRUCTURED_QUERY_SYNTAX, structuredquery/SQS_ADVANCED_QUERY_SYNTAX, structuredquery/SQS_NATURAL_QUERY_SYNTAX, structuredquery/SQS_NO_SYNTAX, structuredquery/STRUCTURED_QUERY_SYNTAX
req.header: structuredquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: STRUCTURED_QUERY_SYNTAX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSTRUCTURED_QUERY_SYNTAX
 - structuredquery/tagSTRUCTURED_QUERY_SYNTAX
 - STRUCTURED_QUERY_SYNTAX
 - structuredquery/STRUCTURED_QUERY_SYNTAX
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
 - STRUCTURED_QUERY_SYNTAX
---

# STRUCTURED_QUERY_SYNTAX enumeration


## -description

Specifies the type of query syntax.

## -enum-fields

### -field SQS_NO_SYNTAX:0

No syntax.

### -field SQS_ADVANCED_QUERY_SYNTAX

Specifies the Advanced Query Syntax. For example, "kind:email to:david to:bill".

### -field SQS_NATURAL_QUERY_SYNTAX

Specifies the Natural Query Syntax. This syntax removes the requirement for a colon between properties and values, for example, "email from david to bill".

## -remarks

Use this enumeration to set the desired SQSO_SYNTAX flag in <a href="/windows/win32/api/structuredquery/ne-structuredquery-structured_query_single_option">STRUCTURED_QUERY_SINGLE_OPTION</a>, which is used with the methods <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-setoption">IQueryParser::SetOption</a> and <a href="/windows/desktop/api/structuredquery/nf-structuredquery-iqueryparser-getoption">IQueryParser::GetOption</a>.
