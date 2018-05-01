---
UID: NN:indexsrv.IWordSink
title: IWordSink
author: windows-driver-content
description: Handles words identified by word breaks during both index time and query time.
old-location: indexsrv\iwordsink.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_55uz.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWordSink, IWordSink interface [Indexing Service], IWordSink interface [Indexing Service], described, _idxs_WordSink, indexsrv.iwordsink, indexsrv/IWordSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IWordSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordSink interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Handles words identified by word breaks during both index time and query time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWordSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWordSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWordSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aead0f02-60ec-46bd-b95d-dd2bce3c6c99">EndAltPhrase</a>
</td>
<td align="left" width="63%">
Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e0d0ec1-1ab9-4cbf-bb28-e38aaa42f41e">PutAltWord</a>
</td>
<td align="left" width="63%">
Puts an alternative word and its position in the WordSink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c14e7c0-bc67-4749-83c2-0484e97762f6">PutBreak</a>
</td>
<td align="left" width="63%">
Puts a break after the preceding word.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3de6e9a7-2213-4401-84a2-7fa73c9d5547">PutWord</a>
</td>
<td align="left" width="63%">
Puts a word and its position in the WordSink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7d0a86e0-59ce-44eb-8df8-40d970b2b363">StartAltPhrase</a>
</td>
<td align="left" width="63%">
Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.

</td>
</tr>
</table> 


## -remarks



Indexing Service creates and initializes instances of the WordSink object. The WordSink receives the <i>fQuery</i> parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.




<a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a> implementations receive a pointer to the WordSink object in the <a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">BreakText</a> method.





