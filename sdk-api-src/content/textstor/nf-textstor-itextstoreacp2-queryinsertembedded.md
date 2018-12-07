---
UID: NF:textstor.ITextStoreACP2.QueryInsertEmbedded
title: ITextStoreACP2::QueryInsertEmbedded
author: windows-sdk-content
description: Gets a value indicating whether the specified object can be inserted into the document.
old-location: tsf\itextstoreacp2_queryinsertembedded.htm
tech.root: TSF
ms.assetid: af67d721-290b-412d-9d99-ea7d6406f33d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],QueryInsertEmbedded method, ITextStoreACP2.QueryInsertEmbedded, ITextStoreACP2::QueryInsertEmbedded, QueryInsertEmbedded, QueryInsertEmbedded method [Text Services Framework], QueryInsertEmbedded method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::QueryInsertEmbedded, tsf.itextstoreacp2_queryinsertembedded
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
 - ITextStoreACP2.QueryInsertEmbedded
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::QueryInsertEmbedded


## -description


Gets a value indicating whether the specified object can be inserted into the document.


## -parameters




### -param pguidService [in]

Pointer to the object type. Can be <b>NULL</b>.


### -param pFormatEtc [in]

Pointer to the <a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a> structure that contains format data of the object. This parameter cannot be <b>NULL</b> if the <i>pguidService</i> parameter is <b>NULL</b>.


### -param pfInsertable [out]

Receives <b>TRUE</b> if the object type can be inserted into the document or <b>FALSE</b> if the object type can't be inserted into the document.


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
The <i>pFormatEtc</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The clipboard formats supported by the document are dependent on the application.




## -see-also




<a href="https://msdn.microsoft.com/4478eb9a-84a1-4f3a-8290-94b8dd20c081">FORMATETC</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/1f5003e0-0d6d-4212-beea-3b2685991749">InsertEmbedded</a>



<a href="https://msdn.microsoft.com/677114a5-8c87-4632-b308-2bb6dedf78c8">InsertEmbeddedAtSelection</a>
 

 

