---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITextStoryRanges2 interface


## -description


The <b>ITextStoryRanges2</b> interface enumerates the stories in an <a href="https://msdn.microsoft.com/0c3f161f-f6d3-44b9-b041-1b682d1915af">ITextDocument</a>.

You get a pointer to an <b>ITextStoryRanges2</b> collection by using the <a href="https://msdn.microsoft.com/e542bd10-228a-4d9a-bd62-c721e56c6369">ITextDocument::GetStoryRanges</a> method. Each story obtained from this collection is represented by an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object that covers the whole story. 

A Text Object Model (TOM) implementation that has only a single story doesn't need to implement the <b>ITextStoryRanges2</b> interface. An implementation of this interface should only retrieve a stories collection if <a href="https://msdn.microsoft.com/6a9d865c-8710-4e67-bf1a-10d09f81488c">ITextDocument::GetStoryCount</a> returns a story count greater than one. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoryRanges2</b> interface inherits from <b>ITextStoryRanges</b>. <b>ITextStoryRanges2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoryRanges2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e77584e-e7ea-44ee-bce8-6f3b84d106bb">Item2</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object for a story, by index, in a stories collection.

</td>
</tr>
</table> 

