---
UID: NN:tom.ITextStoryRanges
title: ITextStoryRanges (tom.h)
author: windows-sdk-content
description: The purpose of the ITextStoryRanges interface is to enumerate the stories in an ITextDocument.
old-location: controls\ITextStoryRanges.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextstoryranges.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoryRanges, ITextStoryRanges interface [Windows Controls], ITextStoryRanges interface [Windows Controls],described, _win32_ITextStoryRanges, _win32_ITextStoryRanges_cpp, controls.ITextStoryRanges, controls._win32_ITextStoryRanges, tom/ITextStoryRanges
ms.topic: interface
f1_keywords: 
 - "tom/ITextStoryRanges"
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextStoryRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextStoryRanges interface


## -description


The purpose of the <b>ITextStoryRanges</b> interface is to enumerate the stories in an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextdocument">ITextDocument</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoryRanges</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextStoryRanges</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoryRanges</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/tom/nf-tom-itextstoryranges-_newenum">_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an 
			<b>IEnumVARIANT</b> enumerator interface for this collection of stories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstoryranges-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of stories in the specified stories collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstoryranges-item">Item</a>
</td>
<td align="left" width="63%">
Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object for the 
			<i>Index</i>th story in this story collection. 

</td>
</tr>
</table> 


## -remarks



 
You get a pointer to an <b>ITextStoryRanges</b> collection by calling the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getstoryranges">GetStoryRanges</a> method. Each story obtained from this collection is represented by an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object that covers the whole story. Text Object Model (TOM) engines that only have a single story do not need to implement an <b>ITextStoryRanges</b> interface. Your code should only get a stories collection if <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextdocument-getstorycount">GetStoryCount</a> returns a story count greater than one.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
 

 

