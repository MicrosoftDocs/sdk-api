---
UID: NF:textstor.ITextStoreACP2.GetSelection
title: ITextStoreACP2::GetSelection
author: windows-sdk-content
description: Gets the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.
old-location: tsf\itextstoreacp2_getselection.htm
tech.root: TSF
ms.assetid: 5f0c6265-7dba-4c59-94f9-36341f05c18d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSelection, GetSelection method [Text Services Framework], GetSelection method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetSelection method, ITextStoreACP2.GetSelection, ITextStoreACP2::GetSelection, textstor/ITextStoreACP2::GetSelection, tsf.itextstoreacp2_getselection
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
 - ITextStoreACP2.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::GetSelection


## -description


Gets the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.


## -parameters




### -param ulIndex [in]

Specifies the text selections that start the process. If the <a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">TF_DEFAULT_SELECTION</a> constant is specified for this parameter, the input selection starts the process.


### -param ulCount [in]

Specifies the maximum number of selections to return.


### -param pSelection [out]

Receives the style, start, and end character positions of the selected text. These values are put into the <a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">TS_SELECTION_ACP</a> structure.


### -param pcFetched [out]

Receives the number of <i>pSelection</i> structures returned.


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
The caller does not have a read-only lock on the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOSELECTION</b></dt>
</dl>
</td>
<td width="60%">
The document has no selection.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/cf8bbe66-d2ad-49b3-9e7c-246e4ca50149">Edit Contexts</a>



<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">ITextStoreACP::SetSelection
      </a>



<a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">Miscellaneous Framework Constants</a>



<a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">TS_SELECTION_ACP
      </a>
 

 

