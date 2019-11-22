---
UID: NF:textstor.ITextStoreACPSink.OnSelectionChange
title: ITextStoreACPSink::OnSelectionChange (textstor.h)

description: ITextStoreACPSink::OnSelectionChange method
old-location: tsf\itextstoreacpsink_onselectionchange.htm
tech.root: TSF
ms.assetid: 500333ae-06dc-4194-a21b-e03c1acc9f9a

ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnSelectionChange method, ITextStoreACPSink.OnSelectionChange, ITextStoreACPSink::OnSelectionChange, OnSelectionChange, OnSelectionChange method [Text Services Framework], OnSelectionChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onselectionchange_ref, textstor/ITextStoreACPSink::OnSelectionChange, tsf.itextstoreacpsink_onselectionchange
ms.topic: method
f1_keywords: 
 - "textstor/ITextStoreACPSink.OnSelectionChange"
dev_langs:
 - c++
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
 - ITextStoreACPSink.OnSelectionChange
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreACPSink::OnSelectionChange


## -description




## -parameters






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
The manager holds a lock on the document.

</td>
</tr>
</table>
 




## -remarks



<b>ITextStoreACPSink::OnSelectionChange</b> is never called when the selection is modified by one of the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> interface methods, such as <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-setselection">ITextStoreACP::SetSelection</a> or <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-inserttextatselection">ITextStoreACP::InsertTextAtSelection</a>.

When calling this method, the application must be able to grant a <a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">document lock</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-inserttextatselection">ITextStoreACP::InsertTextAtSelection
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp-setselection">ITextStoreACP::SetSelection
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>
 

 

