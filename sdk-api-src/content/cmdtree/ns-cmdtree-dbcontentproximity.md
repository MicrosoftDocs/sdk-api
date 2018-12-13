---
UID: NS:cmdtree.tagDBCONTENTPROXIMITY
title: DBCONTENTPROXIMITY
author: windows-sdk-content
description: The DBCONTENTPROXIMITY structure represents specific information required by the DBOP_content_proximity operator.
old-location: indexsrv\dbcontentproximity.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_035l.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DBCONTENTPROXIMITY, DBCONTENTPROXIMITY structure [Indexing Service], _idxs_DBCONTENTPROXIMITY, cmdtree/DBCONTENTPROXIMITY, indexsrv.dbcontentproximity, tagDBCONTENTPROXIMITY
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
 - DBCONTENTPROXIMITY
product: Windows
targetos: Windows
req.typenames: DBCONTENTPROXIMITY
req.redist: 
---

# DBCONTENTPROXIMITY structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBCONTENTPROXIMITY</b> structure represents specific information required by the DBOP_content_proximity operator.


## -struct-fields




### -field dwProximityUnit

words, paras, chapters etc.


### -field ulProximityDistance

how near is "near"?


### -field lWeight

weight of the proximity node


## -remarks



For valid values of the <b>dwProximityUnit</b> member, see <a href="https://msdn.microsoft.com/11c8bfdc-62e7-4404-bb0b-ec47341ec875">Proximity Unit Constants</a>.

For more information on the DBOP_content_proximity operator, see <a href="https://msdn.microsoft.com/aea33c6e-f299-4963-85ae-473963cddfbc">Content Search Operators</a>.



