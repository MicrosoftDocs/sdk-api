---
UID: NF:indexsrv.IWordSink.PutWord
title: IWordSink::PutWord method
author: windows-driver-content
description: Puts a word and its position in the WordSink.
old-location: indexsrv\iwordsink_putword.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_0o2s.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWordSink, IWordSink interface [Indexing Service], PutWord method, IWordSink::PutWord, PutWord method [Indexing Service], PutWord method [Indexing Service], IWordSink interface, PutWord,IWordSink.PutWord, _idxs_WordSink_PutWord, indexsrv.iwordsink_putword, indexsrv/IWordSink::PutWord
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
-	IWordSink.PutWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordSink::PutWord method


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Puts a word and its position in the WordSink.



## -parameters




### -param cwc [in]

The number of characters in <i>pwcInBuf</i>.


### -param pwcInBuf [in]

A pointer to a buffer that contains an alternative form of a word from the source text. This parameter is not modified by <b>PutWord</b>. You can pass the <i>pTextSource</i> parameter from <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">IWordBreaker::BreakText</a> as appropriate.


### -param cwcSrcLen [in]

The number of characters in the source text buffer (indicated by the <i>pTextSource</i> parameter to <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">IWordBreaker::BreakText</a>) that correspond to the word contained in <i>pwcInBuf</i>. 


### -param cwcSrcPos [in]

The starting position of the word in <i>pwcInBuf</i> in the source text buffer (indicated by the <i>pTextSource</i> parameter to <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">IWordBreaker::BreakText</a>). 


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
The operation was completed successfully. Also indicates that no more text is available to refill the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LANGUAGE_S_LARGE_WORD </b></dt>
</dl>
</td>
<td width="60%">
Value of <i>cwc</i> is larger than the value for <i>ulMaxTokenSize</i> that is specified in <a href="https://msdn.microsoft.com/1c9245a9-20f7-42d7-889d-f2eb37f6e2ab">IWordBreaker::Init</a>. 

</td>
</tr>
</table>
 




## -remarks



It is recommended that the <b>PutWord</b> method always contain the original word as found in <i>pTextSource</i>. Alternative forms of the word are passed to WordSink by using <a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">PutAltWord</a>. It is also recommended that the words in <i>pwcInBuf</i> match the source text as closely as possible. For example, retain capitalization and accents where possible.

This call must be made for every word retrieved from <i>pTextSource</i> except those for which the <a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">PutAltWord</a> call was made. The word is terminated with an EOW character when it is saved to the WordSink.




## -see-also




<a href="https://msdn.microsoft.com/0161bc8a-98ba-48b0-8582-b0bcd7b2abe8">IWordSink</a>
 

 

