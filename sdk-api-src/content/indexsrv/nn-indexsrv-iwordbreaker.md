---
UID: NN:indexsrv.IWordBreaker
title: IWordBreaker
author: windows-sdk-content
description: Parses text and identifies individual words and phrases. This interface is a language-specific language resource component. It is used in background processes and must be optimized for both throughput and minimal use of resources.
old-location: search\_search_IWordBreaker.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\iwordbreaker\iwordbreaker.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWordBreaker, IWordBreaker interface [search], IWordBreaker interface [search],described, _search_IWordBreaker, indexsrv/IWordBreaker, search._search_IWordBreaker
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
 - IWordBreaker
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
---

# IWordBreaker interface


## -description


Parses text and identifies individual words and phrases. This interface is a language-specific language resource component. It is used in background processes and must be optimized for both throughput and minimal use of resources.


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
<a href="https://msdn.microsoft.com/32e495c0-e173-4b35-be58-51f31cb38e3e">BreakText</a>
</td>
<td align="left" width="63%">
Parses text to identify words and phrases and provides the results to the <a href="https://msdn.microsoft.com/220FCAE5-D22D-45ED-9689-E78C0D8E0BB3">IWordSink</a> and <a href="https://msdn.microsoft.com/9485202D-94D6-4E9E-9C42-502033E85670">IPhraseSink</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d9f29b8-6a55-4992-94a2-ffffa88cb0bc">ComposePhrase</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b1197bc-7c0d-4c78-8eed-4b6516140d0e">GetLicenseToUse</a>
</td>
<td align="left" width="63%">
Gets a pointer to the license information for this implementation of the <b>IWordBreaker</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7685d85b-de66-4a1e-af54-2a6a42d5de8c">Init</a>
</td>
<td align="left" width="63%">
Initializes the <b>IWordBreaker</b> implementation and indicates the mode in which the component operates.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface to create a custom word breaker for a language. Windows Search calls the methods of this interface when it builds content indexes and runs queries.

Word breaker components for Windows Search run in the Local Security context. They should be written to manage buffers and the stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.



