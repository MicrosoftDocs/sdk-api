---
UID: NS:cmdtree.tagDBCONTENTSCOPE
title: DBCONTENTSCOPE (cmdtree.h)
author: windows-sdk-content
description: The DBCONTENTSCOPE structure is used to pass a scope argument in a command tree.
old-location: indexsrv\dbcontentscope.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_4s85.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DBCONTENTSCOPE, DBCONTENTSCOPE structure [Indexing Service], _idxs_DBCONTENTSCOPE, cmdtree/DBCONTENTSCOPE, indexsrv.dbcontentscope, tagDBCONTENTSCOPE
ms.topic: struct
f1_keywords: 
 - "cmdtree/DBCONTENTSCOPE"
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
 - DBCONTENTSCOPE
product: Windows
targetos: Windows
req.typenames: DBCONTENTSCOPE
req.redist: 
ms.custom: 19H1
---

# DBCONTENTSCOPE structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://docs.microsoft.com/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBCONTENTSCOPE</b> structure is used to pass a scope argument in a command tree.


## -struct-fields




### -field dwFlags

flags from DBPROP_CI_SCOPE_FLAGS


### -field rgpwszTagName

reserved for future use.


### -field pwszElementValue

DBPROP_CI_INCLUDE_SCOPES property for the path

