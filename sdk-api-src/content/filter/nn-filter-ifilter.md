---
UID: NN:filter.IFilter
title: IFilter
author: windows-sdk-content
description: Scans documents for text and properties (also called attributes).
old-location: indexsrv\ifilter.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9sfm.htm
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IFilter, IFilter interface [Indexing Service], IFilter interface [Indexing Service],described, _idxs_IFilter, filter/IFilter, indexsrv.ifilter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: filter.h
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
 - Filter.h
api_name:
 - IFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilter interface


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Scans documents for text and properties (also called attributes). It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text. It also extracts chunks of values, which are properties of an entire document or of well-defined parts of a document. <b>IFilter</b> provides the foundation for building higher-level applications such as document indexers and application-independent viewers.

For introductory information about how the <b>IFilter</b> interface works with documents and document properties, see <a href="https://msdn.microsoft.com/en-us/library/ms689715(v=VS.85).aspx">Properties of Documents</a>. For a synopsis and an example of how the <b>IFilter</b> interface processes a document, see <a href="https://msdn.microsoft.com/en-us/library/ms689681(v=VS.85).aspx">Property Filtering</a> and <a href="https://msdn.microsoft.com/en-us/library/ms689661(v=VS.85).aspx">Property Indexing</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms691053(v=VS.85).aspx">BindRegion</a>
</td>
<td align="left" width="63%">
Retrieves an interface representing the specified portion of object. Currently reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms691080(v=VS.85).aspx">GetChunk</a>
</td>
<td align="left" width="63%">
Positions filter at beginning of first or next chunk and returns a descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690992(v=VS.85).aspx">GetText</a>
</td>
<td align="left" width="63%">
Retrieves text from the current chunk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690927(v=VS.85).aspx">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves values from the current chunk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms690965(v=VS.85).aspx">Init</a>
</td>
<td align="left" width="63%">
Initializes a filtering session.

</td>
</tr>
</table> 


## -remarks



<b>IFilter</b> components for Indexing Service run in the Local Security context and should be written to manage buffers and to stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690929(v=VS.85).aspx">BindIFilterFromStorage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690827(v=VS.85).aspx">BindIFilterFromStream</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691002(v=VS.85).aspx">LoadIFilter</a>
 

 

