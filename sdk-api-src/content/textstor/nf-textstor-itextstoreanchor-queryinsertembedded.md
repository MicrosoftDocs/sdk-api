---
UID: NF:textstor.ITextStoreAnchor.QueryInsertEmbedded
title: ITextStoreAnchor::QueryInsertEmbedded (textstor.h)
author: windows-sdk-content
description: ITextStoreAnchor::QueryInsertEmbedded method
old-location: tsf\itextstoreanchor_queryinsertembedded.htm
tech.root: TSF
ms.assetid: 722506fa-db83-49d3-9434-a4ad7b797ce2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],QueryInsertEmbedded method, ITextStoreAnchor.QueryInsertEmbedded, ITextStoreAnchor::QueryInsertEmbedded, QueryInsertEmbedded, QueryInsertEmbedded method [Text Services Framework], QueryInsertEmbedded method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::QueryInsertEmbedded, tsf.itextstoreanchor_queryinsertembedded
ms.topic: method
f1_keywords: ["textstor/ITextStoreAnchor.QueryInsertEmbedded"]
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITextStoreAnchor.QueryInsertEmbedded
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreAnchor::QueryInsertEmbedded


## -description




## -parameters




### -param pguidService [in]

Pointer to the object type. If <b>NULL</b>, <i>pFormatEtc</i> should be used.


### -param pFormatEtc [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/com/the-formatetc-structure">FORMATETC</a> structure that contains format data of the object. This parameter cannot be <b>NULL</b> if the <i>pguidService</i> parameter is <b>NULL</b>.


### -param pfInsertable [out]

Receives <b>TRUE</b> if the object type can be inserted into the document or <b>FALSE</b> if the object type cannot be inserted into the document.


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




<a href="https://docs.microsoft.com/windows/desktop/com/the-formatetc-structure">FORMATETC</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-insertembedded">ITextStoreAnchor::InsertEmbedded
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-insertembeddedatselection">ITextStoreAnchor::InsertEmbeddedAtSelection
      </a>
 

 

