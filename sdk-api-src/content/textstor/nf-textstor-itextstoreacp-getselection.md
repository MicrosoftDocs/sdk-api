---
UID: NF:textstor.ITextStoreACP.GetSelection
title: ITextStoreACP::GetSelection (textstor.h)
author: windows-sdk-content
description: The ITextStoreACP::GetSelection method returns the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.
old-location: tsf\itextstoreacp_getselection.htm
tech.root: TSF
ms.assetid: e2052daf-4168-4266-ae8d-a09ecbfeb422
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Text Services Framework], GetSelection method [Text Services Framework],ITextStoreACP interface, ITextStoreACP interface [Text Services Framework],GetSelection method, ITextStoreACP.GetSelection, ITextStoreACP::GetSelection, _tsf_itextstoreacp_getselection_ref, textstor/ITextStoreACP::GetSelection, tsf.itextstoreacp_getselection
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP.GetSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreACP::GetSelection


## -description


The <b>ITextStoreACP::GetSelection</b> method returns the character position of a text selection in a document. This method supports multiple text selections. The caller must have a read-only lock on the document before calling this method.


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



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/e9151b63-2ca7-4995-a36b-b919ab2d491a">ITextStoreACP::SetSelection
      </a>



<a href="https://msdn.microsoft.com/fa53c1f1-50eb-45eb-b2ea-f236a376d41a">Miscellaneous Framework Constants</a>



<a href="https://msdn.microsoft.com/739c87c5-3e9c-41f3-ad79-0b417347604b">TS_SELECTION_ACP
      </a>
 

 

