---
UID: NE:indexsrv.tagWORDREP_BREAK_TYPE
title: tagWORDREP_BREAK_TYPE
author: windows-sdk-content
description: Describes the type of break that separates the current word from the previous word.
old-location: indexsrv\wordrep_break_type.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_12at.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WORDREP_BREAK_EOC, WORDREP_BREAK_EOP, WORDREP_BREAK_EOS, WORDREP_BREAK_EOW, WORDREP_BREAK_TYPE, WORDREP_BREAK_TYPE enumeration [Indexing Service], _idxs_WORDREP_BREAK_TYPE, indexsrv.wordrep_break_type, indexsrv/WORDREP_BREAK_EOC, indexsrv/WORDREP_BREAK_EOP, indexsrv/WORDREP_BREAK_EOS, indexsrv/WORDREP_BREAK_EOW, indexsrv/WORDREP_BREAK_TYPE, tagWORDREP_BREAK_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: indexsrv.h
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
 - Indexsrv.h
api_name:
 - WORDREP_BREAK_TYPE
product: Windows
targetos: Windows
req.typenames: WORDREP_BREAK_TYPE
req.redist: 
---

# tagWORDREP_BREAK_TYPE enumeration


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Describes the type of break that separates the current word from the previous word.


## -enum-fields




### -field WORDREP_BREAK_EOW

A word break is placed between this word and the previous word that was placed in the <b>WordSink</b>. This break is the default used by the <a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">PutWord</a> method.


### -field WORDREP_BREAK_EOS

A sentence break is placed between this word and the previous word.


### -field WORDREP_BREAK_EOP

A paragraph break is placed between this word and the previous word. 


### -field WORDREP_BREAK_EOC

A chapter break is placed between this word and the previous word.


## -see-also




<a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">IWordSink::PutAltWord</a>



<a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">IWordSink::PutWord</a>
 

 

