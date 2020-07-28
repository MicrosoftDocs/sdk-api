---
UID: NS:cmdtree.tagDBCONTENTPROXIMITY
title: DBCONTENTPROXIMITY (cmdtree.h)
description: The DBCONTENTPROXIMITY structure represents specific information required by the DBOP_content_proximity operator.
helpviewer_keywords: ["DBCONTENTPROXIMITY","DBCONTENTPROXIMITY structure [Indexing Service]","_idxs_DBCONTENTPROXIMITY","cmdtree/DBCONTENTPROXIMITY","indexsrv.dbcontentproximity","tagDBCONTENTPROXIMITY"]
old-location: indexsrv\dbcontentproximity.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_035l.htm
ms.date: 12/05/2018
ms.keywords: DBCONTENTPROXIMITY, DBCONTENTPROXIMITY structure [Indexing Service], _idxs_DBCONTENTPROXIMITY, cmdtree/DBCONTENTPROXIMITY, indexsrv.dbcontentproximity, tagDBCONTENTPROXIMITY
f1_keywords:
- cmdtree/DBCONTENTPROXIMITY
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
- DBCONTENTPROXIMITY
targetos: Windows
req.typenames: DBCONTENTPROXIMITY
req.redist: 
ms.custom: 19H1
---

# DBCONTENTPROXIMITY structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

The <b>DBCONTENTPROXIMITY</b> structure represents specific information required by the DBOP_content_proximity operator.


## -struct-fields




### -field dwProximityUnit

words, paras, chapters etc.


### -field ulProximityDistance

how near is "near"?


### -field lWeight

weight of the proximity node


## -remarks



For valid values of the <b>dwProximityUnit</b> member, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/proximity-unit-constants">Proximity Unit Constants</a>.

For more information on the DBOP_content_proximity operator, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/content-search-operators">Content Search Operators</a>.



