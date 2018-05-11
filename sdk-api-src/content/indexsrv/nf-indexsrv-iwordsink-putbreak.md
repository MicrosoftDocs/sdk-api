---
UID: NF:indexsrv.IWordSink.PutBreak
title: IWordSink::PutBreak
author: windows-driver-content
description: Puts a break after the preceding word.
old-location: indexsrv\iwordsink_putbreak.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_71kb.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWordSink interface [Indexing Service],PutBreak method, IWordSink.PutBreak, IWordSink::PutBreak, PutBreak, PutBreak method [Indexing Service], PutBreak method [Indexing Service],IWordSink interface, _idxs_WordSink_PutBreak, indexsrv.iwordsink_putbreak, indexsrv/IWordSink::PutBreak
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WORDREP_BREAK_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Indexsrv.h
api_name:
-	IWordSink.PutBreak
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordSink::PutBreak


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Puts a break after the preceding word.


## -parameters




### -param breakType [in]

A value from <a href="https://msdn.microsoft.com/bdc7e588-2de4-45a0-aa4a-56424f1b34d0">WORDREP_BREAK_TYPE</a> that indicates the type of break that the WordSink inserts after the preceding word. Each break occupies a unique position in the index. Therefore, inserting breaks between words changes the relative distance between words.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was completed successfully.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">PutWord</a> and <a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">PutAltWord</a> methods automatically insert an end-of-word break (EOW, indicated by the WORDREP_BREAK_EOW element of the <a href="https://msdn.microsoft.com/bdc7e588-2de4-45a0-aa4a-56424f1b34d0">WORDREP_BREAK_TYPE</a> enumerated type) after each word. Call the <b>PutBreak</b> method to insert a break type other than end of word. This method does not change the source text buffer (<i>pSourceText</i>) or increment the character count (<i>cwc</i>). However, it does increment the current position in the index and affects query results.




## -see-also




<a href="https://msdn.microsoft.com/0161bc8a-98ba-48b0-8582-b0bcd7b2abe8">IWordSink</a>
 

 

