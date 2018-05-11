---
UID: NF:indexsrv.IWordSink.StartAltPhrase
title: IWordSink::StartAltPhrase
author: windows-driver-content
description: Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.
old-location: indexsrv\iwordsink_startaltphrase.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_0945.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWordSink interface [Indexing Service],StartAltPhrase method, IWordSink.StartAltPhrase, IWordSink::StartAltPhrase, StartAltPhrase, StartAltPhrase method [Indexing Service], StartAltPhrase method [Indexing Service],IWordSink interface, _idxs_WordSink_StartAltPhrase, indexsrv.iwordsink_startaltphrase, indexsrv/IWordSink::StartAltPhrase
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
-	IWordSink.StartAltPhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordSink::StartAltPhrase


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.



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

<a href="https://msdn.microsoft.com/7d0a86e0-59ce-44eb-8df8-40d970b2b363">StartAltPhrase</a> is called during query time.

</td>
</tr>
</table>
 




## -remarks



Each alternative phrase starts with a <b>StartAltPhrase</b> call. The phrase is put in the WordSink through subsequent calls to the <a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">PutWord</a> or <a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">PutAltWord</a> method. The final alternative phrase in a sequence of phrases is terminated with a call to the <a href="https://msdn.microsoft.com/aead0f02-60ec-46bd-b95d-dd2bce3c6c99">EndAltPhrase</a> method.






## -see-also




<a href="https://msdn.microsoft.com/0161bc8a-98ba-48b0-8582-b0bcd7b2abe8">IWordSink</a>
 

 

