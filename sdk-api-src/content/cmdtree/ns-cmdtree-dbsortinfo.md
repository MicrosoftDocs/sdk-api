---
UID: NS:cmdtree.tagDBSORTINFO
title: DBSORTINFO (cmdtree.h)
description: The DBSORTINFO structure stores the order in which a column will be sorted (that is, ascending or descending). This information is stored inside a DBOP_sort_list_element node.
helpviewer_keywords: ["DBSORTINFO","DBSORTINFO structure [Indexing Service]","_idxs_DBSORTINFO","cmdtree/DBSORTINFO","indexsrv.dbsortinfo","tagDBSORTINFO"]
old-location: indexsrv\dbsortinfo.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2mpb.htm
ms.date: 12/05/2018
ms.keywords: DBSORTINFO, DBSORTINFO structure [Indexing Service], _idxs_DBSORTINFO, cmdtree/DBSORTINFO, indexsrv.dbsortinfo, tagDBSORTINFO
req.header: cmdtree.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: DBSORTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBSORTINFO
 - cmdtree/tagDBSORTINFO
 - DBSORTINFO
 - cmdtree/DBSORTINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cmdtree.h
api_name:
 - DBSORTINFO
---

# DBSORTINFO structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBSORTINFO</b> structure stores the order in which a column will be sorted (that is, ascending or descending). This information is stored inside a DBOP_sort_list_element node.

## -struct-fields

### -field fDesc

TRUE = ascending, FALSE = descending

### -field lcid

locale identifier

## -remarks

The locale identifier (LCID) specifies a set of user preference information related to the user's language. It determines how times are formatted, how items are alphabetically sorted, and how strings are compared.

For additional information on LCIDs see <a href="/previous-versions/ms776264(v=vs.85)">Locales</a>.