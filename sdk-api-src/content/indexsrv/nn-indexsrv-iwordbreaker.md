---
UID: NN:indexsrv.IWordBreaker
title: IWordBreaker
author: windows-driver-content
description: The IWordBreaker interface is a language-specific language resource component.
old-location: indexsrv\iwordbreaker.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_93xu.htm
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IWordBreaker, IWordBreaker interface [Indexing Service], IWordBreaker interface [Indexing Service],described, _idxs_IWordBreaker, indexsrv.iwordbreaker, indexsrv/IWordBreaker
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
-	IWordBreaker
-	IWordBreaker.ComposePhrase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IWordBreaker interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

The <b>IWordBreaker</b> interface is a language-specific language resource component. The word breaker parses text and identifies individual words and phrases. The word breaker is used in background processes and must be optimized for both throughput and minimal use of resources.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWordBreaker</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWordBreaker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWordBreaker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25d84f9a-502d-4187-9dbf-6aca7cb74562">BreakText</a>
</td>
<td align="left" width="63%">
Breaks text to identify words and phrases and provides the results to the WordSink and PhraseSink objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>ComposePhrase</b></td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e79b017d-ca88-4e4d-b3d1-b1c046143e86">GetLicenseToUse</a>
</td>
<td align="left" width="63%">
Retrieves the license information for this <b>IWordBreaker</b> implementation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541624">Init</a>
</td>
<td align="left" width="63%">
Initializes the <b>IWordBreaker</b> implementation and indicates the mode in which the component operates.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c257db30-821a-44c0-8896-890090c9aedf">Implementing a Word Breaker</a>



<a href="https://msdn.microsoft.com/48241f14-3dba-4b55-947a-fd636361ed1e">Language Resource Samples</a>
 

 

