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

# ITextStoreACP::QueryInsert


## -description


The <b>ITextStoreACP::QueryInsert</b> method determines whether the specified start and end character positions are valid. Use this method to adjust an edit to a document before executing the edit. The method must not return values outside the range of the document.


## -parameters




### -param acpTestStart [in]

Starting application character position for inserted text.


### -param acpTestEnd [in]

Ending application character position for the inserted text. This value is equal to <i>acpTextStart</i> if the text is inserted at a point instead of replacing selected text.


### -param cch [in]

Length of replacement text.


### -param pacpResultStart [out]

Returns the new starting application character position of the inserted text. If this parameter is <b>NULL</b>, then text cannot be inserted at the specified position. This value cannot be outside the document range.


### -param pacpResultEnd [out]

Returns the new ending application character position of the inserted text. If this parameter is <b>NULL</b>, then <i>pacpResultStart</i> is set to <b>NULL</b> and text cannot be inserted at the specified position. This value cannot be outside the document range.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>acpTestStart</i> or <i>acpTestEnd</i> parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



The values of <i>pacpResultStart</i> and <i>pacpResultEnd</i> depend upon how the application inserts text into the document. If <i>pacpResultStart</i> and <i>pacpResultEnd</i> are the same as <i>acpTextStart</i>, the cursor is at the beginning of the inserted text after insertion. If <i>pacpResultStart</i> and <i>pacpResultEnd</i> are the same as <i>acpTextEnd</i>, the cursor is at the end of the inserted text after insertion. If the difference between <i>pacpResultStart</i> and <i>pacpResultEnd</i> is equal to the length of the inserted text, the inserted text is highlighted after insertion.



