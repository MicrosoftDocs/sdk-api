---
UID: NS:cmdtree.tagDBCONTENT
title: DBCONTENT (cmdtree.h)
description: The DBCONTENT structure represents specific information required by the DBOP_content operator.
helpviewer_keywords: ["DBCONTENT","DBCONTENT structure [Indexing Service]","_idxs_DBCONTENT","cmdtree/DBCONTENT","indexsrv.dbcontent","tagDBCONTENT"]
old-location: indexsrv\dbcontent.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_569g.htm
ms.date: 12/05/2018
ms.keywords: DBCONTENT, DBCONTENT structure [Indexing Service], _idxs_DBCONTENT, cmdtree/DBCONTENT, indexsrv.dbcontent, tagDBCONTENT
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
req.typenames: DBCONTENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBCONTENT
 - cmdtree/tagDBCONTENT
 - DBCONTENT
 - cmdtree/DBCONTENT
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
 - DBCONTENT
---

# DBCONTENT structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBCONTENT</b> structure represents specific information required by the DBOP_content operator.

## -struct-fields

### -field pwszPhrase

text

### -field dwGenerateMethod

exact, prefix, stemmed

### -field lWeight

weight of node

### -field lcid

locale

## -remarks

For valid values of the <b>dwGenerateMethod</b> member, see <a href="/previous-versions/windows/desktop/indexsrv/generate-method-constants">Generate Method Constants</a>.

For more information on the DBOP_content operator, see <a href="/previous-versions/windows/desktop/indexsrv/content-search-operators">Content Search Operators</a>.