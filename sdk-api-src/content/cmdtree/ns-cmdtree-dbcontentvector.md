---
UID: NS:cmdtree.tagDBCONTENTVECTOR
title: DBCONTENTVECTOR (cmdtree.h)
description: The DBCONTENTVECTOR structure represents specific information required by the DBOP_content_vector_or operator.
helpviewer_keywords: ["DBCONTENTVECTOR","DBCONTENTVECTOR structure [Indexing Service]","_idxs_DBCONTENTVECTOR","cmdtree/DBCONTENTVECTOR","indexsrv.dbcontentvector","tagDBCONTENTVECTOR"]
old-location: indexsrv\dbcontentvector.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_0coi.htm
ms.date: 12/05/2018
ms.keywords: DBCONTENTVECTOR, DBCONTENTVECTOR structure [Indexing Service], _idxs_DBCONTENTVECTOR, cmdtree/DBCONTENTVECTOR, indexsrv.dbcontentvector, tagDBCONTENTVECTOR
f1_keywords:
- cmdtree/DBCONTENTVECTOR
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- cmdtree.h
api_name:
- DBCONTENTVECTOR
targetos: Windows
req.typenames: DBCONTENTVECTOR
req.redist: 
ms.custom: 19H1
---

## -description

<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

The <b>DBCONTENTVECTOR</b> structure represents specific information required by the DBOP_content_vector_or operator.

## -struct-fields

### -field lWeight

Node weight.

### -field dwRankingMethod

Jaccard, dice, and so on.

## -remarks

For valid values of the <b>dwRankingMethod</b> member, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/vector-rank-constants">Vector Rank Constants</a>.

For more information on the DBOP_content_vector operator, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/content-search-operators">Content Search Operators</a>.
