---
UID: NN:tom.ITextStory
title: ITextStory (tom.h)
description: The ITextStory interface methods are used to access shared data from multiple stories, which is stored in the parent ITextServices instance.
helpviewer_keywords: ["ITextStory","ITextStory interface [Windows Controls]","ITextStory interface [Windows Controls]","described","controls.itextstory","tom/ITextStory"]
old-location: controls\itextstory.htm
tech.root: Controls
ms.assetid: 8b52c6e8-c250-4cfb-979e-770df9f94010
ms.date: 12/05/2018
ms.keywords: ITextStory, ITextStory interface [Windows Controls], ITextStory interface [Windows Controls],described, controls.itextstory, tom/ITextStory
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStory
 - tom/ITextStory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory
---

# ITextStory interface


## -description

The <b>ITextStory</b> interface methods are used to access shared data from multiple stories, which is stored in the parent <a href="https://docs.microsoft.com/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a> instance. 

The stories can be "edited" simultaneously by using individual <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> methods, and displayed independently of one another. In addition, one story at a time can be UI active; that is, it receives keyboard and mouse input. 


The <b>ITextStory</b> is a lightweight interface that does not require an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object. This allows the client to manipulate a story, which is a faster, smaller object than a complete editing instance.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextStory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-getactive">GetActive</a>
</td>
<td align="left" width="63%">
Sets the active state of a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-getdisplay">GetDisplay</a>
</td>
<td align="left" width="63%">
Gets a new display for a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh768726(v=vs.85)">GetIndex</a>
</td>
<td align="left" width="63%">
Gets the index of a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-getrange">GetRange</a>
</td>
<td align="left" width="63%">
Gets a text range object for the story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-gettext">GetText</a>
</td>
<td align="left" width="63%">
Gets the text in a story according to the specified conversion flags. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets this story's type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-setactive">SetActive</a>
</td>
<td align="left" width="63%">
Sets the active state of a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-setformattedtext">SetFormattedText</a>
</td>
<td align="left" width="63%">
Replaces a story’s text with specified formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-settext">SetText</a>
</td>
<td align="left" width="63%">
Replaces the text in a story with the specified text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstory-settype">SetType</a>
</td>
<td align="left" width="63%">
Sets the story type.

</td>
</tr>
</table>

