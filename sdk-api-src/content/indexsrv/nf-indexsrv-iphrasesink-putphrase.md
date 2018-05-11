---
UID: NF:indexsrv.IPhraseSink.PutPhrase
title: IPhraseSink::PutPhrase
author: windows-driver-content
description: Puts a query-time phrase in the PhraseSink.
old-location: indexsrv\iphrasesink_putphrase.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_8n8l.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IPhraseSink interface [Indexing Service],PutPhrase method, IPhraseSink.PutPhrase, IPhraseSink::PutPhrase, PutPhrase, PutPhrase method [Indexing Service], PutPhrase method [Indexing Service],IPhraseSink interface, _idxs_PhraseSink_PutPhrase, indexsrv.iphrasesink_putphrase, indexsrv/IPhraseSink::PutPhrase
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
-	IPhraseSink.PutPhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPhraseSink::PutPhrase


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Puts a query-time phrase in the PhraseSink.



## -parameters




### -param pwcPhrase [in]

A pointer to a buffer that contains a phrase.


### -param cwcPhrase [in]

The number of characters in <i>pwcPhrase</i>. There is no limit on the size of a query-time phrase.


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
<tr>
<td width="40%">
<dl>
<dt><b>PSINK_E_QUERY_ONLY </b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/86bff25f-190c-48f9-abd8-29dceb3e9912">PutPhrase</a> was called at index time instead of query time.

</td>
</tr>
</table>
 




## -remarks



<b>PutPhrase</b> is called by the <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">BreakText</a> method of the <a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> implementation. Phrases that the PhraseSink object handles are used by the Indexing Service to expand the original query text.






## -see-also




<a href="https://msdn.microsoft.com/4226f3d3-b7e4-43a3-838f-0da6bebf51ea">IPhraseSink</a>
 

 

