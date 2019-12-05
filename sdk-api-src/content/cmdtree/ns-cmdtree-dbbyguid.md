---
UID: NS:cmdtree.tagDBBYGUID
title: DBBYGUID (cmdtree.h)
description: The DBBYGUID structure supplies supplementary information for a node.
old-location: indexsrv\dbbyguid.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_32xw.htm
ms.date: 12/05/2018
ms.keywords: DBBYGUID, DBBYGUID structure [Indexing Service], _idxs_DBBYGUID, cmdtree/DBBYGUID, indexsrv.dbbyguid, tagDBBYGUID
ms.topic: struct
f1_keywords:
- cmdtree/DBBYGUID
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
- DBBYGUID
targetos: Windows
req.typenames: DBBYGUID
req.redist: 
ms.custom: 19H1
---

# DBBYGUID structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBBYGUID</b> structure supplies supplementary information for a node.


## -struct-fields




### -field pbInfo

extra node information, provider-specific


### -field cbInfo

size of the data in pbInfo


### -field guid

this node's GUID


## -remarks



The information stored in the <b>pbInfo</b> member is provider-specific, and provides for operation extensibility.



