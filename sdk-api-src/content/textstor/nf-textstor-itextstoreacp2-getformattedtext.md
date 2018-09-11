---
UID: NF:textstor.ITextStoreACP2.GetFormattedText
title: ITextStoreACP2::GetFormattedText
author: windows-sdk-content
description: Gets formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.
old-location: tsf\itextstoreacp2_getformattedtext.htm
tech.root: TSF
ms.assetid: 0993861d-ef2a-4da5-a564-7559e7c4dcec
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFormattedText, GetFormattedText method [Text Services Framework], GetFormattedText method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetFormattedText method, ITextStoreACP2.GetFormattedText, ITextStoreACP2::GetFormattedText, textstor/ITextStoreACP2::GetFormattedText, tsf.itextstoreacp2_getformattedtext
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.GetFormattedText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::GetFormattedText


## -description


Gets formatted text data about a specified text string. The caller must have a read/write lock on the document before calling this method.


## -parameters




### -param acpStart [in]

Specifies the starting character position of the text to get in the document.


### -param acpEnd [in]

Specifies the ending character position of the text to get in the document. This parameter is ignored if the value is 1.


### -param ppDataObject [out]

Receives the pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> object that contains the formatted text.


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
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock on the document.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>
 

 

