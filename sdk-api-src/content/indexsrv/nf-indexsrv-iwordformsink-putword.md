---
UID: NF:indexsrv.IWordFormSink.PutWord
title: IWordFormSink::PutWord method
author: windows-driver-content
description: Puts the original word form in the WordFormSink.
old-location: indexsrv\iwordformsink_putword.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_7qlg.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IWordFormSink, IWordFormSink interface [Indexing Service], PutWord method, IWordFormSink::PutWord, PutWord method [Indexing Service], PutWord method [Indexing Service], IWordFormSink interface, PutWord,IWordFormSink.PutWord, _idxs_StemSink_PutWord, indexsrv.iwordformsink_putword, indexsrv/IWordFormSink::PutWord
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
-	IWordFormSink.PutWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordFormSink::PutWord method


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Puts the original word form in the WordFormSink.



## -parameters




### -param pwcInBuf [in]

 A pointer to a buffer that contains the final alternative form of a word. 


### -param cwc [in]

The number of characters in <i>pwcInBuf</i>. 


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



<b>PutWord</b> is called from the <a href="https://msdn.microsoft.com/944c3776-3b92-4f41-8b85-7f27b2779177">GenerateWordForms</a> method of the <a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a> implementation. This method handles the original form of a word and is called last. All preceding alternative forms for a word are put in the WordFormSink by calling <a href="https://msdn.microsoft.com/9e286de4-eebf-43df-871c-bd8d6add2bd6">PutAltWord</a>.






## -see-also




<a href="https://msdn.microsoft.com/da4abc7f-f196-46de-be69-0064d527f792">IWordFormSink</a>
 

 

