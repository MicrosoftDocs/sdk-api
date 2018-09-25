---
UID: NN:indexsrv.IPhraseSink
title: IPhraseSink
author: windows-sdk-content
description: Handles phrases that word breakers parse from query text during query time.
old-location: indexsrv\iphrasesink.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefobj_3asr.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IPhraseSink, IPhraseSink interface [Indexing Service], IPhraseSink interface [Indexing Service],described, _idxs_PhraseSink, indexsrv.iphrasesink, indexsrv/IPhraseSink
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Indexsrv.h
api_name:
 - IPhraseSink
 - IPhraseSink.PutSmallPhrase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhraseSink interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Handles phrases that word breakers parse from query text during query time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhraseSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhraseSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhraseSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86bff25f-190c-48f9-abd8-29dceb3e9912">PutPhrase</a>
</td>
<td align="left" width="63%">
Puts a query-time phrase in the PhraseSink object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>PutSmallPhrase</b></td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
</table> 


## -remarks



Indexing Service creates and initializes instances of the PhraseSink object. The PhraseSink receives the <i>fQuery</i> parameter during initialization and uses this parameter to determine the word-breaking context in which the object is being used.




<a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a> implementations receive a pointer to the PhraseSink object in the <a href="https://msdn.microsoft.com/en-us/library/Bb266429(v=VS.85).aspx">BreakText</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb266433(v=VS.85).aspx">IWordBreaker</a>
 

 

