---
UID: NE:cmdtree.DBCOMMANDREUSEENUM
title: DBCOMMANDREUSEENUM
author: windows-sdk-content
description: The DBCOMMANDREUSEENUM enumerated type specifies whether a state from the previous command is retained.
old-location: indexsrv\dbcommandreuseenum.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_71v1.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DBCOMMANDREUSEENUM, DBCOMMANDREUSEENUM enumeration [Indexing Service], DBCOMMANDREUSE_NONE, DBCOMMANDREUSE_PARAMETERS, DBCOMMANDREUSE_PROPERTIES, _idxs_DBCOMMANDREUSEENUM, cmdtree/DBCOMMANDREUSEENUM, cmdtree/DBCOMMANDREUSE_NONE, cmdtree/DBCOMMANDREUSE_PARAMETERS, cmdtree/DBCOMMANDREUSE_PROPERTIES, indexsrv.dbcommandreuseenum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
 - DBCOMMANDREUSEENUM
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DBCOMMANDREUSEENUM enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBCOMMANDREUSEENUM</b> enumerated type specifies whether a state from the previous command is retained.


## -enum-fields




### -field DBCOMMANDREUSE_NONE


### -field DBCOMMANDREUSE_PROPERTIES


### -field DBCOMMANDREUSE_PARAMETERS


## -remarks



The <a href="https://msdn.microsoft.com/13161978-498d-4a55-ba28-b15c66cf966f">ICommandTree::SetCommandTree</a> method uses a value from this enumerated type as a parameter.



