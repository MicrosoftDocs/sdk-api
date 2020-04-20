---
UID: NS:cmdtree.tagDBSETFUNC
title: DBSETFUNC (cmdtree.h)
description: The DBSETFUNC structure specifies the aggregation function to use in a select operation.helpviewer_keywords: ["DBSETFUNC","DBSETFUNC structure [Indexing Service]","_idxs_DBSETFUNC","cmdtree/DBSETFUNC","indexsrv.dbsetfunc","tagDBSETFUNC"]
old-location: indexsrv\dbsetfunc.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_5e1v.htm
ms.date: 12/05/2018
ms.keywords: DBSETFUNC, DBSETFUNC structure [Indexing Service], _idxs_DBSETFUNC, cmdtree/DBSETFUNC, indexsrv.dbsetfunc, tagDBSETFUNC
f1_keywords:
- cmdtree/DBSETFUNC
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
- DBSETFUNC
targetos: Windows
req.typenames: DBSETFUNC
req.redist: 
ms.custom: 19H1
---

# DBSETFUNC structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="https://www.microsoft.com/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

The <b>DBSETFUNC</b> structure specifies the aggregation function to use in a select operation.


## -struct-fields




### -field dwSetQuantifier

which aggregation method to use


## -remarks



For valid values of the <b>dwSetQuantifier</b> member, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/indexsrv/aggregate-function-constants">Aggregate Function Constants</a>.



