---
UID: NS:cmdtree.tagDBCONTENTSCOPE
title: DBCONTENTSCOPE (cmdtree.h)
description: The DBCONTENTSCOPE structure is used to pass a scope argument in a command tree.
helpviewer_keywords: ["DBCONTENTSCOPE","DBCONTENTSCOPE structure [Indexing Service]","_idxs_DBCONTENTSCOPE","cmdtree/DBCONTENTSCOPE","indexsrv.dbcontentscope","tagDBCONTENTSCOPE"]
old-location: indexsrv\dbcontentscope.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_4s85.htm
ms.date: 12/05/2018
ms.keywords: DBCONTENTSCOPE, DBCONTENTSCOPE structure [Indexing Service], _idxs_DBCONTENTSCOPE, cmdtree/DBCONTENTSCOPE, indexsrv.dbcontentscope, tagDBCONTENTSCOPE
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
req.typenames: DBCONTENTSCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBCONTENTSCOPE
 - cmdtree/tagDBCONTENTSCOPE
 - DBCONTENTSCOPE
 - cmdtree/DBCONTENTSCOPE
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
 - DBCONTENTSCOPE
---

# DBCONTENTSCOPE structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBCONTENTSCOPE</b> structure is used to pass a scope argument in a command tree.

## -struct-fields

### -field dwFlags

flags from DBPROP_CI_SCOPE_FLAGS

### -field rgpwszTagName

reserved for future use.

### -field pwszElementValue

DBPROP_CI_INCLUDE_SCOPES property for the path