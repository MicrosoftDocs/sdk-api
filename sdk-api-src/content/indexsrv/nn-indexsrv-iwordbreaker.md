---
UID: NN:indexsrv.IWordBreaker
title: IWordBreaker (indexsrv.h)

description: Parses text and identifies individual words and phrases. This interface is a language-specific language resource component. It is used in background processes and must be optimized for both throughput and minimal use of resources.
old-location: search\_search_IWordBreaker.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\iwordbreaker\iwordbreaker.htm

ms.date: 12/05/2018
ms.keywords: IWordBreaker, IWordBreaker interface [search], IWordBreaker interface [search],described, _search_IWordBreaker, indexsrv/IWordBreaker, search._search_IWordBreaker
ms.topic: interface
f1_keywords: 
 - "indexsrv/IWordBreaker"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
ms.custom: 19H1
---

# IWordBreaker interface


## -description


Parses text and identifies individual words and phrases. This interface is a language-specific language resource component. It is used in background processes and must be optimized for both throughput and minimal use of resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWordBreaker</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWordBreaker</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext">BreakText</a>
</td>
<td align="left" width="63%">
Parses text to identify words and phrases and provides the results to the <a href="https://docs.microsoft.com/windows/desktop/search/iwordsink">IWordSink</a> and <a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nn-indexsrv-iphrasesink">IPhraseSink</a> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-composephrase">ComposePhrase</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-getlicensetouse">GetLicenseToUse</a>
</td>
<td align="left" width="63%">
Gets a pointer to the license information for this implementation of the <b>IWordBreaker</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/indexsrv/nf-indexsrv-iwordbreaker-init">Init</a>
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



