---
UID: NS:cmdtree.tagDBSETFUNC
title: DBSETFUNC
author: windows-sdk-content
description: The DBSETFUNC structure specifies the aggregation function to use in a select operation.
old-location: indexsrv\dbsetfunc.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_5e1v.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DBSETFUNC, DBSETFUNC structure [Indexing Service], _idxs_DBSETFUNC, cmdtree/DBSETFUNC, indexsrv.dbsetfunc, tagDBSETFUNC
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DBSETFUNC
product: Windows
targetos: Windows
req.typenames: DBSETFUNC
req.redist: 
---

# DBSETFUNC structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBSETFUNC</b> structure specifies the aggregation function to use in a select operation.


## -struct-fields




### -field dwSetQuantifier

which aggregation method to use


## -remarks



For valid values of the <b>dwSetQuantifier</b> member, see <a href="https://msdn.microsoft.com/b9b4ea13-9db7-498e-b62f-acbe76c2bb3b">Aggregate Function Constants</a>.



