---
UID: NN:tom.ITextStory
title: ITextStory
author: windows-sdk-content
description: The ITextStory interface methods are used to access shared data from multiple stories, which is stored in the parent ITextServices instance.
old-location: controls\itextstory.htm
old-project: Controls
ms.assetid: 8b52c6e8-c250-4cfb-979e-770df9f94010
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITextStory, ITextStory interface [Windows Controls], ITextStory interface [Windows Controls],described, controls.itextstory, tom/ITextStory
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
req.idl: Tom.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tom.h
api_name:
 - ITextStory
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStory interface


## -description


The <b>ITextStory</b> interface methods are used to access shared data from multiple stories, which is stored in the parent <a href="https://msdn.microsoft.com/en-us/library/Bb787617(v=VS.85).aspx">ITextServices</a> instance. 

The stories can be "edited" simultaneously by using individual <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> methods, and displayed independently of one another. In addition, one story at a time can be UI active; that is, it receives keyboard and mouse input. 


The <b>ITextStory</b> is a lightweight interface that does not require an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object. This allows the client to manipulate a story, which is a faster, smaller object than a complete editing instance.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7bae9458-ee68-486a-a37f-2cc899400882">GetActive</a>
</td>
<td align="left" width="63%">
Sets the active state of a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9ea7fbc-b814-4dbd-ae8a-9e260b56abab">GetDisplay</a>
</td>
<td align="left" width="63%">
Gets a new display for a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef7f4714-6887-429c-8f65-77c14d55a5c4">GetIndex</a>
</td>
<td align="left" width="63%">
Gets the index of a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c24e9d8-c737-42f8-87d9-585b0054b6df">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cc02056-c431-470a-83ef-99e47123da1e">GetRange</a>
</td>
<td align="left" width="63%">
Gets a text range object for the story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926850">GetText</a>
</td>
<td align="left" width="63%">
Gets the text in a story according to the specified conversion flags. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Gets this story's type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa0177be-2016-4205-b121-921dbdbf5b71">SetActive</a>
</td>
<td align="left" width="63%">
Sets the active state of a story.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddc77bfe-06de-43e6-9d74-f1b3531c9416">SetFormattedText</a>
</td>
<td align="left" width="63%">
Replaces a story’s text with specified formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/432afe58-a1ed-45aa-b018-bf608bbb7e2a">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9efd45ed-00f7-47e1-90e7-82a420e79bdf">SetText</a>
</td>
<td align="left" width="63%">
Replaces the text in a story with the specified text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991816">SetType</a>
</td>
<td align="left" width="63%">
Sets the story type.

</td>
</tr>
</table> 

