---
UID: NS:cmdtree.tagDBLIKE
title: DBLIKE
author: windows-sdk-content
description: The DBLIKE structure represents specific information required by the DBOP_like operator.
old-location: indexsrv\dblike.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_84rp.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DBLIKE, DBLIKE structure [Indexing Service], _idxs_DBLIKE, cmdtree/DBLIKE, indexsrv.dblike, tagDBLIKE
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
 - DBLIKE
product: Windows
targetos: Windows
req.typenames: DBLIKE
req.redist: 
---

# DBLIKE structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBLIKE</b> structure represents specific information required by the DBOP_like operator.


## -struct-fields




### -field lWeight

weight on the dbop_like node


### -field guidDialect

system to use for "likeness". E.g. Reg. Ex.


## -remarks



For more information about the DBOP_like operator, see <a href="https://msdn.microsoft.com/en-us/library/ms690350(v=VS.85).aspx">Operators for Scalars</a>. 



