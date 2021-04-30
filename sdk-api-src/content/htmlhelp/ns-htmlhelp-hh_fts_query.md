---
UID: NS:htmlhelp.tagHH_FTS_QUERY
title: HH_FTS_QUERY (htmlhelp.h)
description: Use this structure for full-text search.
helpviewer_keywords: ["HH_FTS_QUERY","HH_FTS_QUERY structure [HTML Help Workshop]","htmlhelp.hh_fts_query_structure","htmlhelp/HH_FTS_QUERY","vsconStrhhftsquery"]
old-location: htmlhelp\hh_fts_query_structure.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\vsconstrhhftsquery.htm
ms.date: 12/05/2018
ms.keywords: HH_FTS_QUERY, HH_FTS_QUERY structure [HTML Help Workshop], htmlhelp.hh_fts_query_structure, htmlhelp/HH_FTS_QUERY, vsconStrhhftsquery
req.header: htmlhelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: HH_FTS_QUERY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagHH_FTS_QUERY
 - htmlhelp/tagHH_FTS_QUERY
 - HH_FTS_QUERY
 - htmlhelp/HH_FTS_QUERY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HtmlHelp.h
api_name:
 - HH_FTS_QUERY
---

# HH_FTS_QUERY structure


## -description

Use this structure for full-text search.

## -struct-fields

### -field cbStruct

Specifies the size of the structure.

### -field fUniCodeStrings

TRUE if all strings are Unicode.

### -field pszSearchQuery

String containing the search query.

### -field iProximity

Word proximity.

### -field fStemmedSearch

TRUE for StemmedSearch only.

### -field fTitleOnly

TRUE for Title search only.

### -field fExecute

TRUE to initiate the search.

### -field pszWindow

Window to display in.

## -see-also

<a href="/previous-versions/windows/desktop/htmlhelp/about-structures">About Structures</a>