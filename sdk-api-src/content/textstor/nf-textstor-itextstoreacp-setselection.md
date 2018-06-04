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

# ITextStoreACP::SetSelection


## -description


The <b>ITextStoreACP::SetSelection</b> method selects text within the document. The application must have a read/write lock on the document before calling this method.


## -parameters




### -param ulCount [in]

Specifies the number of text selections in <i>pSelection</i>.


### -param pSelection [in]

Specifies the style, start, and end character positions of the text selected through the <a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">TS_SELECTION_ACP</a> structure.

When the start and end character positions are equal, the method places a caret at that character position. There can be only one caret at a time in the document.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The character positions specified are beyond the text in the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/e2052daf-4168-4266-ae8d-a09ecbfeb422">
        ITextStoreACP::GetSelection
      </a>



<a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">TS_SELECTION_ACP
      </a>
 

 

