---
UID: NN:peninputpanel.IHandwrittenTextInsertion
title: IHandwrittenTextInsertion (peninputpanel.h)
author: windows-sdk-content
description: Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.
old-location: tablet\ihandwrittentextinsertion.htm
tech.root: tablet
ms.assetid: 67fcf19a-a864-40de-987f-406f18726a9f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 67fcf19a-a864-40de-987f-406f18726a9f, IHandWrittenTextInsertion, IHandWrittenTextInsertion interface [Tablet PC], IHandWrittenTextInsertion interface [Tablet PC],described, peninputpanel/IHandWrittenTextInsertion, tablet.ihandwrittentextinsertion
ms.topic: interface
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Tiptsf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tiptsf.dll
api_name:
 - IHandWrittenTextInsertion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHandwrittenTextInsertion interface


## -description



Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHandWrittenTextInsertion</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHandWrittenTextInsertion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHandWrittenTextInsertion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d519aff4-573d-4b06-aef5-e9cc6a5e8102">InsertInkRecognitionResult</a>
</td>
<td align="left" width="63%">
Insert recognition results.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3566d1c-e4fb-4f0d-9beb-0b5e5db66985">InsertRecognitionResultsArray</a>
</td>
<td align="left" width="63%">
Insert recognition results array.

</td>
</tr>
</table> 


## -remarks



This element is declared in Peninputpanel.h.



