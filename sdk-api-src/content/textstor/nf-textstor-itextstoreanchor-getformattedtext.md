---
UID: NF:textstor.ITextStoreAnchor.GetFormattedText
title: ITextStoreAnchor::GetFormattedText
author: windows-sdk-content
description: The ITextStoreAnchor::GetFormattedText method returns formatted text information from a text stream.
old-location: tsf\itextstoreanchor_getformattedtext.htm
old-project: TSF
ms.assetid: 2b104b0a-b900-4acb-801e-d9716e3a0146
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetFormattedText, GetFormattedText method [Text Services Framework], GetFormattedText method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetFormattedText method, ITextStoreAnchor.GetFormattedText, ITextStoreAnchor::GetFormattedText, textstor/ITextStoreAnchor::GetFormattedText, tsf.itextstoreanchor_getformattedtext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreAnchor.GetFormattedText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchor::GetFormattedText


## -description


The <b>ITextStoreAnchor::GetFormattedText</b> method returns formatted text information from a text stream.


## -parameters




### -param paStart [in]

Anchor position at which to start retrieval of formatted text.


### -param paEnd [in]

Anchor position at which to end retrieval of formatted text.


### -param ppDataObject [out]

Pointer to the <a href="_ole_idataobject">IDataObject</a> object that contains the formatted text.


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
The method was unable to obtain a valid interface pointer to the start and/or end anchors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
An application can return this value if the method is not implemented.

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
 




## -remarks



Text, embedded objects, and any formatting are wrapped into a single <b>IDataObject</b> object. In this way private appliation-specific formatting associated with text can be preserved by a client.




## -see-also




<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>
 

 

