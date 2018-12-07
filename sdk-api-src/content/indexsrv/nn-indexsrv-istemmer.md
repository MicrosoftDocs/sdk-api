---
UID: NN:indexsrv.IStemmer
title: IStemmer
author: windows-sdk-content
description: Provides methods for creating a language-specific stemmer. The stemmer generates inflected forms of a specified word.
old-location: search\_search_IStemmer.htm
tech.root: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\dataaddins\istemmer\istemmer.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStemmer, IStemmer interface [search], IStemmer interface [search],described, _search_IStemmer, indexsrv/IStemmer, search._search_IStemmer
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
 - IStemmer
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows NT 4.0 Option Pack
---

# IStemmer interface


## -description


Provides methods for creating a language-specific stemmer. The stemmer generates inflected forms of a specified word.


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
<a href="https://msdn.microsoft.com/en-us/library/Bb266434(v=VS.85).aspx">GenerateWordForms</a>
</td>
<td align="left" width="63%">
Generates alternative forms for a word and puts these forms in the <a href="https://msdn.microsoft.com/81D52B0C-BADD-48C0-85DB-57CA82D7BBA8">IWordFormSink</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266435(v=VS.85).aspx">GetLicenseToUse</a>
</td>
<td align="left" width="63%">
Gets the license information for this <b>IStemmer</b> implementation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb266436(v=VS.85).aspx">Init</a>
</td>
<td align="left" width="63%">
Initializes the stemmer.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface to create a custom stemmer for a language. Windows Search calls the methods of this interface to generate inflected forms for words identified when building an index.

Stemmer components for Windows Search run in the Local Security context. They should be written to manage buffers and the stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.



