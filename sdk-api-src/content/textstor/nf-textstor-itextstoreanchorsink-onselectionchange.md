---
UID: NF:textstor.ITextStoreAnchorSink.OnSelectionChange
title: ITextStoreAnchorSink::OnSelectionChange (textstor.h)
author: windows-sdk-content
description: The ITextStoreAnchorSink::OnSelectionChange method is called when the selection within the text stream changes. This method should be called whenever the return value of a potential call to ITextStoreAnchor::GetSelection has changed.
old-location: tsf\itextstoreanchorsink_onselectionchange.htm
tech.root: TSF
ms.assetid: e33932b0-f5ce-4325-809d-ec06cb4a49a6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnSelectionChange method, ITextStoreAnchorSink.OnSelectionChange, ITextStoreAnchorSink::OnSelectionChange, OnSelectionChange, OnSelectionChange method [Text Services Framework], OnSelectionChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onselectionchange_ref, textstor/ITextStoreAnchorSink::OnSelectionChange, tsf.itextstoreanchorsink_onselectionchange
ms.topic: method
f1_keywords: 
 - "textstor/ITextStoreAnchorSink.OnSelectionChange"
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
 - ITextStoreAnchorSink.OnSelectionChange
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITextStoreAnchorSink::OnSelectionChange


## -description


The <b>ITextStoreAnchorSink::OnSelectionChange</b> method is called when the selection within the text stream changes. This method should be called whenever the return value of a potential call to <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-getselection">ITextStoreAnchor::GetSelection</a> has changed.


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



This method only needs to be called when the application modifies the selection itself, not when a client modifies the selection with <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-setselection">ITextStoreAnchor::SetSelection</a>, <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-inserttextatselection">ITextStoreAnchor::InsertTextAtSelection</a>, or other <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a> methods.

When calling this method, the application must be able to grant a <a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">document lock</a>.

Applications should expect reentrant client calls to <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestlock">ITextStoreAnchor::RequestLock</a> from within this method. An application can grant the lock request synchronously, or, because several changes have been cached, it can grant the lock asynchronously.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TSF/document-locks">Document Locks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-inserttextatselection">ITextStoreAnchor::InsertTextAtSelection
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-setselection">ITextStoreAnchor::SetSelection
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreanchorsink">ITextStoreAnchorSink</a>
 

 

