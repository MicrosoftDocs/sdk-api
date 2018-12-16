---
UID: NS:cmdtree.tagDBTEXT
title: DBTEXT
author: windows-sdk-content
description: The DBTEXT structure is used by the DBOP_text_command node.
old-location: indexsrv\dbtext.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_2qyc.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DBTEXT, DBTEXT structure [Indexing Service], _idxs_DBTEXT, cmdtree/DBTEXT, indexsrv.dbtext, tagDBTEXT
ms.topic: struct
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
 - DBTEXT
product: Windows
targetos: Windows
req.typenames: DBTEXT
req.redist: 
---

# DBTEXT structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

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



For additional information about the <i>guidDialect</i> parameter, see the description of DBOP_text_command in <a href="https://msdn.microsoft.com/en-us/library/ms689751(v=VS.85).aspx">Special Operators</a>.



