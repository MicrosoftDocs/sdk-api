---
UID: NE:searchapi._SEARCH_QUERY_SYNTAX
title: SEARCH_QUERY_SYNTAX (searchapi.h)
description: Specifies the type of query syntax.
helpviewer_keywords: ["SEARCH_ADVANCED_QUERY_SYNTAX","SEARCH_NATURAL_QUERY_SYNTAX","SEARCH_NO_QUERY_SYNTAX","SEARCH_QUERY_SYNTAX","SEARCH_QUERY_SYNTAX enumeration [search]","_search_SEARCH_QUERY_SYNTAX","search._search_SEARCH_QUERY_SYNTAX","searchapi/SEARCH_ADVANCED_QUERY_SYNTAX","searchapi/SEARCH_NATURAL_QUERY_SYNTAX","searchapi/SEARCH_NO_QUERY_SYNTAX","searchapi/SEARCH_QUERY_SYNTAX"]
old-location: search\_search_SEARCH_QUERY_SYNTAX.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\enums\search_query_syntax.htm
ms.date: 12/05/2018
ms.keywords: SEARCH_ADVANCED_QUERY_SYNTAX, SEARCH_NATURAL_QUERY_SYNTAX, SEARCH_NO_QUERY_SYNTAX, SEARCH_QUERY_SYNTAX, SEARCH_QUERY_SYNTAX enumeration [search], _search_SEARCH_QUERY_SYNTAX, search._search_SEARCH_QUERY_SYNTAX, searchapi/SEARCH_ADVANCED_QUERY_SYNTAX, searchapi/SEARCH_NATURAL_QUERY_SYNTAX, searchapi/SEARCH_NO_QUERY_SYNTAX, searchapi/SEARCH_QUERY_SYNTAX
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SEARCH_QUERY_SYNTAX
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - _SEARCH_QUERY_SYNTAX
 - searchapi/_SEARCH_QUERY_SYNTAX
 - SEARCH_QUERY_SYNTAX
 - searchapi/SEARCH_QUERY_SYNTAX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Searchapi.h
api_name:
 - SEARCH_QUERY_SYNTAX
---

# SEARCH_QUERY_SYNTAX enumeration


## -description

Specifies the type of query syntax.

## -enum-fields

### -field SEARCH_NO_QUERY_SYNTAX:0

No syntax.

### -field SEARCH_ADVANCED_QUERY_SYNTAX

Specifies the Advanced Query Syntax. For example, "kind:email to:david to:bill".

### -field SEARCH_NATURAL_QUERY_SYNTAX

Specifies the Natural Query Syntax. This syntax removes the requirement for a colon between properties and values, for example, "email from david to bill".

## -remarks

This enumerated type is used by the <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax">ISearchQueryHelper::get_QuerySyntax</a> and <a href="/windows/desktop/api/searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax">ISearchQueryHelper::put_QuerySyntax</a> methods.

<div class="alert"><b>Note</b>   In Windows 7, the names are prefixed with SQS_ instead of SEARCH_.</div>
<div> </div>
