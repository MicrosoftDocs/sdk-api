---
UID: NN:indexsrv.IPhraseSink
title: IPhraseSink
author: windows-sdk-content
description: Handles phrases that word breakers parse from query text during query time.
old-location: search\iphrasesink.htm
tech.root: search
ms.assetid: 9485202D-94D6-4E9E-9C42-502033E85670
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IPhraseSink, IPhraseSink interface [search], IPhraseSink interface [search],described, indexsrv/IPhraseSink, search.iphrasesink
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
<a href="https://msdn.microsoft.com/5E1762A8-8CC9-4EAE-BC79-91672994C1E3">PutPhrase</a>
</td>
<td align="left" width="63%">
Puts a query-time phrase in the <b>IPhraseSink</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">PutSmallPhrase</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
</table> 


## -remarks



Windows Search creates and initializes instances of the <b>IPhraseSink</b> object. The <b>IPhraseSink</b> object receives the <i>fQuery</i> parameter during initialization and uses this parameter to determine the word-breaking context in which the object is being used.




<a href="https://msdn.microsoft.com/36c46931-5c5c-4ab9-9291-60ad93cebbf0">IWordBreaker</a> implementations receive a pointer to the <b>IPhraseSink</b> object in the <a href="https://msdn.microsoft.com/32e495c0-e173-4b35-be58-51f31cb38e3e">IWordBreaker::BreakText</a> method.



