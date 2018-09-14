---
UID: NN:filter.IFilter
title: IFilter
author: windows-sdk-content
description: Scans documents for text and properties (also called attributes).
old-location: indexsrv\ifilter.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9sfm.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IFilter, IFilter interface [Indexing Service], IFilter interface [Indexing Service],described, _idxs_IFilter, filter/IFilter, indexsrv.ifilter
ms.prod: windows
ms.technology: windows-sdk
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


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Scans documents for text and properties (also called attributes). It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text. It also extracts chunks of values, which are properties of an entire document or of well-defined parts of a document. <b>IFilter</b> provides the foundation for building higher-level applications such as document indexers and application-independent viewers.

For introductory information about how the <b>IFilter</b> interface works with documents and document properties, see <a href="https://msdn.microsoft.com/103ddfc0-b431-4a52-bf3a-acaf39e34bc2">Properties of Documents</a>. For a synopsis and an example of how the <b>IFilter</b> interface processes a document, see <a href="https://msdn.microsoft.com/bb8884fb-ffe1-4e07-879e-9febe7dbbfab">Property Filtering</a> and <a href="https://msdn.microsoft.com/0474da14-8fdf-4f93-a21b-d8f7edb9fcde">Property Indexing</a>.




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
<a href="https://msdn.microsoft.com/d4ee07f3-4260-4b33-9ac9-436d17c80f2c">BindRegion</a>
</td>
<td align="left" width="63%">
Retrieves an interface representing the specified portion of object. Currently reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d4f3150-deec-40b6-a945-b4cea241db8d">GetChunk</a>
</td>
<td align="left" width="63%">
Positions filter at beginning of first or next chunk and returns a descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d63639a6-6729-44cd-8105-198a268ff2d6">GetText</a>
</td>
<td align="left" width="63%">
Retrieves text from the current chunk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91d53ef4-06bb-4756-acc2-723cf041959b">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves values from the current chunk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cb9b675-258e-46b0-905f-15a086f84f74">Init</a>
</td>
<td align="left" width="63%">
Initializes a filtering session.

</td>
</tr>
</table> 


## -remarks



<b>IFilter</b> components for Indexing Service run in the Local Security context and should be written to manage buffers and to stack correctly. All string copies must have explicit checks to guard against buffer overruns. You should always verify the allocated size of the buffer and test the size of the data against the size of the buffer.




## -see-also




<a href="https://msdn.microsoft.com/b8d9657e-f910-4beb-b35d-b69c7b3544ad">BindIFilterFromStorage</a>



<a href="https://msdn.microsoft.com/6f0d3e15-a3b6-4299-95fe-e0c38ce11aa6">BindIFilterFromStream</a>



<a href="https://msdn.microsoft.com/08d8bb9d-97f8-4d21-adbb-65c927612d19">LoadIFilter</a>
 

 

