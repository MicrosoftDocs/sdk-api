---
UID: NN:indexsrv.IWordFormSink
title: IWordFormSink
author: windows-driver-content
description: Handles the list of alternative word forms that stemmers generate during query time.
old-location: indexsrv\iwordformsink.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_2z1n.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWordFormSink, IWordFormSink interface [Indexing Service], IWordFormSink interface [Indexing Service], described, _idxs_StemSink, indexsrv.iwordformsink, indexsrv/IWordFormSink
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
-	IWordFormSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordFormSink interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Handles the list of alternative word forms that stemmers generate during query time.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWordFormSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWordFormSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWordFormSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e286de4-eebf-43df-871c-bd8d6add2bd6">PutAltWord</a>
</td>
<td align="left" width="63%">
Puts an alternative form of a word in the WordFormSink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7ec20fb-1362-4fc0-be5a-7035fa4b3ed5">PutWord</a>
</td>
<td align="left" width="63%">
Puts the original word form in the WordFormSink.

</td>
</tr>
</table> 


## -remarks



Indexing Service creates and initializes instances of the StemSink object. The WordFormSink receives the <i>ulMaxTokenSize</i> parameter during initialization. The value for this parameter is determined by the <a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a> implementation and determines the maximum length, in characters, for a single word that the WordFormSink handles.




<a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a> implementations receive a pointer to the WordFormSink object in the <a href="https://msdn.microsoft.com/944c3776-3b92-4f41-8b85-7f27b2779177">GenerateWordForms</a> method.






## -see-also




<a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a>
 

 

