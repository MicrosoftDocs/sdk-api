---
UID: NF:textstor.ITextStoreACP2.InsertEmbedded
title: ITextStoreACP2::InsertEmbedded
author: windows-sdk-content
description: Inserts an embedded object at the specified character.
old-location: tsf\itextstoreacp2_insertembedded.htm
tech.root: TSF
ms.assetid: 1f5003e0-0d6d-4212-beea-3b2685991749
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],InsertEmbedded method, ITextStoreACP2.InsertEmbedded, ITextStoreACP2::InsertEmbedded, InsertEmbedded, InsertEmbedded method [Text Services Framework], InsertEmbedded method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::InsertEmbedded, tsf.itextstoreacp2_insertembedded
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
 - ITextStoreACP2.InsertEmbedded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::InsertEmbedded


## -description


Inserts an embedded object at the specified character.


## -parameters




### -param dwFlags [in]

Must be TS_IE_CORRECTION.


### -param acpStart [in]

Contains the starting character position where the object is inserted.


### -param acpEnd [in]

Contains the ending character position where the object is inserted.


### -param pDataObject [in]

Pointer to an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface that contains data about the object inserted.


### -param pChange [out]

Pointer to a <a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE</a> structure that receives data about the modified text.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The application does not support embedded objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The application does not support the data type contained in <i>pDataObject</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
<i>acpStart</i> and/or <i>acpEnd</i> are not within the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read/write lock.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/a455d712-42d5-472e-862d-85ae3ba9149f">TS_IE_* Constants
      </a>



<a href="https://msdn.microsoft.com/af7dfc32-ae2d-4f04-a73b-8a9e2ea1a1c0">TS_TEXTCHANGE
      </a>
 

 

