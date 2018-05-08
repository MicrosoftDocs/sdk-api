---
UID: NF:indexsrv.IWordFormSink.PutAltWord
title: IWordFormSink::PutAltWord
author: windows-driver-content
description: Puts an alternative form of a word in the WordFormSink.
old-location: indexsrv\iwordformsink_putaltword.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_64is.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWordFormSink interface [Indexing Service],PutAltWord method, IWordFormSink.PutAltWord, IWordFormSink::PutAltWord, PutAltWord, PutAltWord method [Indexing Service], PutAltWord method [Indexing Service],IWordFormSink interface, _idxs_IStemSink_PutAltWord, indexsrv.iwordformsink_putaltword, indexsrv/IWordFormSink::PutAltWord
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
-	IWordFormSink.PutAltWord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordFormSink::PutAltWord


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Puts an alternative form of a word in the WordFormSink.



## -parameters




### -param pwcInBuf [in]

A pointer to a buffer that contains an alternative form of a word. 



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
<tr>
<td width="40%">
<dl>
<dt><b>LANGUAGE_S_LARGE_WORD </b></dt>
</dl>
</td>
<td width="60%">
Value of <i>cwc</i> is larger than the value for <i>ulMaxTokenSize</i> that is specified in <a href="https://msdn.microsoft.com/3d11708c-4a0a-46b0-ac48-5976cdca4a36">IStemmer::Init</a>. 

</td>
</tr>
</table>
 




## -remarks



This method is called from the <a href="https://msdn.microsoft.com/944c3776-3b92-4f41-8b85-7f27b2779177">GenerateWordForms</a> method of the <a href="https://msdn.microsoft.com/3b655078-367d-4e74-aeb1-a5b5c135e88e">IStemmer</a> implementation. All alternative forms for a word, except the last, are put in the WordFormSink by calling <b>PutAltWord</b>. The final alternative form of a word is handled by calling <a href="https://msdn.microsoft.com/f7ec20fb-1362-4fc0-be5a-7035fa4b3ed5">PutWord</a>.






## -see-also




<a href="https://msdn.microsoft.com/da4abc7f-f196-46de-be69-0064d527f792">IWordFormSink</a>
 

 

