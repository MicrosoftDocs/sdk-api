---
UID: NE:cmdtree.DBCOMMANDREUSEENUM
title: DBCOMMANDREUSEENUM (cmdtree.h)
description: The DBCOMMANDREUSEENUM enumerated type specifies whether a state from the previous command is retained.
helpviewer_keywords: ["DBCOMMANDREUSEENUM","DBCOMMANDREUSEENUM enumeration [Indexing Service]","DBCOMMANDREUSE_NONE","DBCOMMANDREUSE_PARAMETERS","DBCOMMANDREUSE_PROPERTIES","_idxs_DBCOMMANDREUSEENUM","cmdtree/DBCOMMANDREUSEENUM","cmdtree/DBCOMMANDREUSE_NONE","cmdtree/DBCOMMANDREUSE_PARAMETERS","cmdtree/DBCOMMANDREUSE_PROPERTIES","indexsrv.dbcommandreuseenum"]
old-location: indexsrv\dbcommandreuseenum.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_71v1.htm
ms.date: 12/05/2018
ms.keywords: DBCOMMANDREUSEENUM, DBCOMMANDREUSEENUM enumeration [Indexing Service], DBCOMMANDREUSE_NONE, DBCOMMANDREUSE_PARAMETERS, DBCOMMANDREUSE_PROPERTIES, _idxs_DBCOMMANDREUSEENUM, cmdtree/DBCOMMANDREUSEENUM, cmdtree/DBCOMMANDREUSE_NONE, cmdtree/DBCOMMANDREUSE_PARAMETERS, cmdtree/DBCOMMANDREUSE_PROPERTIES, indexsrv.dbcommandreuseenum
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DBCOMMANDREUSEENUM
 - cmdtree/DBCOMMANDREUSEENUM
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
 - DBCOMMANDREUSEENUM
---

# DBCOMMANDREUSEENUM enumeration


## -description

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

The <b>DBCOMMANDREUSEENUM</b> enumerated type specifies whether a state from the previous command is retained.

## -enum-fields

### -field DBCOMMANDREUSE_NONE:0

### -field DBCOMMANDREUSE_PROPERTIES:0x1

### -field DBCOMMANDREUSE_PARAMETERS:0x2

## -remarks

The <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">ICommandTree::SetCommandTree</a> method uses a value from this enumerated type as a parameter.
