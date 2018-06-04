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



