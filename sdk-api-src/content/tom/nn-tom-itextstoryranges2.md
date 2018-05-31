---
UID: NN:tom.ITextStoryRanges2
title: ITextStoryRanges2
author: windows-sdk-content
description: The ITextStoryRanges2 interface enumerates the stories in an ITextDocument.
old-location: controls\itextstoryranges2.htm
old-project: Controls
ms.assetid: 24e2dd79-8054-44e3-aa68-778a96e2f66a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ITextStoryRanges2, ITextStoryRanges2 interface [Windows Controls], ITextStoryRanges2 interface [Windows Controls],described, controls.itextstoryranges2, tom/ITextStoryRanges2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextStoryRanges2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
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

