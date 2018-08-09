---
UID: NF:textstor.ITextStoreACP2.QueryInsert
title: ITextStoreACP2::QueryInsert
author: windows-sdk-content
description: Determines whether the specified start and end character positions are valid. Use this method to adjust an edit to a document before executing the edit. The method must not return values outside the range of the document.
old-location: tsf\itextstoreacp2_queryinsert.htm
old-project: TSF
ms.assetid: 3a1cf233-5185-414a-99c6-2cfdbe07b8c9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],QueryInsert method, ITextStoreACP2.QueryInsert, ITextStoreACP2::QueryInsert, QueryInsert, QueryInsert method [Text Services Framework], QueryInsert method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::QueryInsert, tsf.itextstoreacp2_queryinsert
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TsRunType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.QueryInsert
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP2::QueryInsert


## -description


Determines whether the specified start and end character positions are valid. Use this method to adjust an edit to a document before executing the edit. The method must not return values outside the range of the document.


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




## -see-also




<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>
 

 

