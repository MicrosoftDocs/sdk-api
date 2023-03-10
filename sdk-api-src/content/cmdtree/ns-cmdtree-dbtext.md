---
UID: NS:cmdtree.tagDBTEXT
title: DBTEXT (cmdtree.h)
description: The DBTEXT structure is used by the DBOP_text_command node.
helpviewer_keywords: ["DBTEXT","DBTEXT structure [Indexing Service]","_idxs_DBTEXT","cmdtree/DBTEXT","indexsrv.dbtext","tagDBTEXT"]
old-location: indexsrv\dbtext.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2qyc.htm
ms.date: 12/05/2018
ms.keywords: DBTEXT, DBTEXT structure [Indexing Service], _idxs_DBTEXT, cmdtree/DBTEXT, indexsrv.dbtext, tagDBTEXT
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
req.typenames: DBTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDBTEXT
 - cmdtree/tagDBTEXT
 - DBTEXT
 - cmdtree/DBTEXT
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
 - DBTEXT
---

# DBTEXT structure


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBTEXT</b> structure is used by the DBOP_text_command node. It stores the dialect to use to interpret the string stored in the <b>pwszText</b> member. The error locator is filled in by the provider, that is, the first offending token is indicated as the index into the text array, together with its length.

## -struct-fields

### -field pwszText

### -field ulErrorLocator

set by validation routines

### -field ulTokenLength

length of offending token

### -field guidDialect

lGUID of the language and dialect

## -remarks

For additional information about the <i>guidDialect</i> parameter, see the description of DBOP_text_command in <a href="/previous-versions/windows/desktop/indexsrv/special-operators">Special Operators</a>.