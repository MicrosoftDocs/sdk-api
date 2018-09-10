---
UID: NS:cmdtree.tagDBCONTENTVECTOR
title: tagDBCONTENTVECTOR
author: windows-sdk-content
description: The DBCONTENTVECTOR structure represents specific information required by the DBOP_content_vector_or operator.
old-location: indexsrv\dbcontentvector.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixoledb_0coi.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DBCONTENTVECTOR, DBCONTENTVECTOR structure [Indexing Service], _idxs_DBCONTENTVECTOR, cmdtree/DBCONTENTVECTOR, indexsrv.dbcontentvector, tagDBCONTENTVECTOR
ms.prod: windows
ms.technology: windows-sdk
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
 - DBCONTENTVECTOR
product: Windows
targetos: Windows
req.typenames: DBCONTENTVECTOR
req.redist: 
---

# tagDBCONTENTVECTOR structure


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>DBCONTENTVECTOR</b> structure represents specific information required by the DBOP_content_vector_or operator.


## -struct-fields




### -field lWeight

 


### -field dwRankingMethod

jaccard, dice, etc.


#### - lWeights

node weight


## -remarks



For valid values of the <b>dwRankingMethod</b> member, see <a href="https://msdn.microsoft.com/dc495ce3-4cae-48a9-8193-f13b64c3cc01">Vector Rank Constants</a>.

For more information on the DBOP_content_vector operator, see <a href="https://msdn.microsoft.com/aea33c6e-f299-4963-85ae-473963cddfbc">Content Search Operators</a>. 



