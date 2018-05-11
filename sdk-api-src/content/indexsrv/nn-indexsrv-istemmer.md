---
UID: NN:indexsrv.IStemmer
title: IStemmer
author: windows-driver-content
description: Provides methods for creating a language-specific stemmer. The stemmer generates inflected forms of a given word.
old-location: indexsrv\istemmer.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_4b76.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IStemmer, IStemmer interface [Indexing Service], IStemmer interface [Indexing Service],described, _idxs_IStemmer, indexsrv.istemmer, indexsrv/IStemmer
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
-	IStemmer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStemmer interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Provides methods for creating a language-specific stemmer. The stemmer generates inflected forms of a given word.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStemmer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStemmer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStemmer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/944c3776-3b92-4f41-8b85-7f27b2779177">GenerateWordForms</a>
</td>
<td align="left" width="63%">
Generates alternative forms for a word and puts them in the WordFormSink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d0812a6-679c-4163-aab7-60d0283d7c2c">GetLicenseToUse</a>
</td>
<td align="left" width="63%">
Gets the license information for this <b>IStemmer</b> implementation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the stemmer.

</td>
</tr>
</table> 


## -remarks



Stemmer components for Indexing Service run in the Local Security context. They should be written to manage buffers and to stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.




## -see-also




<a href="https://msdn.microsoft.com/994befe1-e258-4c0a-b3a9-b5968e13456c">IWordBreaker</a>



<a href="https://msdn.microsoft.com/d8ace103-a4ca-424f-9358-cd5fc6263a87">Implementing a Stemmer</a>



<a href="https://msdn.microsoft.com/48241f14-3dba-4b55-947a-fd636361ed1e">Language Resource Samples</a>
 

 

