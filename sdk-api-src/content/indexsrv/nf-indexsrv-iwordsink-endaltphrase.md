---
UID: NF:indexsrv.IWordSink.EndAltPhrase
title: IWordSink::EndAltPhrase
author: windows-driver-content
description: Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.
old-location: indexsrv\iwordsink_endaltphrase.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_5j51.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: EndAltPhrase, EndAltPhrase method [Indexing Service], EndAltPhrase method [Indexing Service],IWordSink interface, IWordSink interface [Indexing Service],EndAltPhrase method, IWordSink.EndAltPhrase, IWordSink::EndAltPhrase, _idxs_WordSink_EndAltPhrase, indexsrv.iwordsink_endaltphrase, indexsrv/IWordSink::EndAltPhrase
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
-	IWordSink.EndAltPhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordSink::EndAltPhrase


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.



## -parameters






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
<dt><b>WBREAK_E_QUERY_ONLY</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/aead0f02-60ec-46bd-b95d-dd2bce3c6c99">EndAltPhrase</a> is called during query time.

</td>
</tr>
</table>
 




## -remarks




<a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> implementations call <b>EndAltPhrase</b> from their <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">BreakText</a> method to terminate a sequence of alternative phrases. The <a href="https://msdn.microsoft.com/7d0a86e0-59ce-44eb-8df8-40d970b2b363">StartAltPhrase</a> method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases. Only the last phrase in a sequence is terminated with a call to <b>EndAltPhrase</b>.






## -see-also




<a href="https://msdn.microsoft.com/0161bc8a-98ba-48b0-8582-b0bcd7b2abe8">IWordSink</a>
 

 

