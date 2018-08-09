---
UID: NF:textstor.ITextStoreACP2.SetSelection
title: ITextStoreACP2::SetSelection
author: windows-sdk-content
description: Selects text within the document. The application must have a read/write lock on the document before calling this method.
old-location: tsf\itextstoreacp2_setselection.htm
old-project: TSF
ms.assetid: 0ed72ddd-523e-476a-ba4c-bbfef9483015
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],SetSelection method, ITextStoreACP2.SetSelection, ITextStoreACP2::SetSelection, SetSelection, SetSelection method [Text Services Framework], SetSelection method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::SetSelection, tsf.itextstoreacp2_setselection
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
 - ITextStoreACP2.SetSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP2::SetSelection


## -description


Selects text within the document. The application must have a read/write lock on the document before calling this method.


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




<a href="https://msdn.microsoft.com/5f0c6265-7dba-4c59-94f9-36341f05c18d">GetSelection</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">TS_SELECTION_ACP</a>
 

 

