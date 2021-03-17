---
UID: NS:cmdtree.tagDBCONTENTTABLE
title: DBCONTENTTABLE (cmdtree.h)
description: The DBCONTENTTABLE structure represents the machine and catalog names for a command tree.
helpviewer_keywords: ["DBCONTENTTABLE","DBCONTENTTABLE structure [Indexing Service]","_idxs_DBCONTENTTABLE","cmdtree/DBCONTENTTABLE","indexsrv.dbcontenttable","tagDBCONTENTTABLE"]
old-location: indexsrv\dbcontenttable.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_1zs5.htm
ms.date: 12/05/2018
ms.keywords: DBCONTENTTABLE, DBCONTENTTABLE structure [Indexing Service], _idxs_DBCONTENTTABLE, cmdtree/DBCONTENTTABLE, indexsrv.dbcontenttable, tagDBCONTENTTABLE
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
req.typenames: DBCONTENTTABLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBCONTENTTABLE
 - cmdtree/tagDBCONTENTTABLE
 - DBCONTENTTABLE
 - cmdtree/DBCONTENTTABLE
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
 - DBCONTENTTABLE
---

# DBCONTENTTABLE structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBCONTENTTABLE</b> structure represents the machine and catalog names for a command tree.

## -struct-fields

### -field pwszMachine

machine on which to process query

### -field pwszCatalog

catalog over which to process query