---
UID: NF:textstor.ITextStoreAnchorSink.OnSelectionChange
title: ITextStoreAnchorSink::OnSelectionChange
author: windows-sdk-content
description: The ITextStoreAnchorSink::OnSelectionChange method is called when the selection within the text stream changes. This method should be called whenever the return value of a potential call to ITextStoreAnchor::GetSelection has changed.
old-location: tsf\itextstoreanchorsink_onselectionchange.htm
tech.root: TSF
ms.assetid: e33932b0-f5ce-4325-809d-ec06cb4a49a6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITextStoreAnchorSink interface [Text Services Framework],OnSelectionChange method, ITextStoreAnchorSink.OnSelectionChange, ITextStoreAnchorSink::OnSelectionChange, OnSelectionChange, OnSelectionChange method [Text Services Framework], OnSelectionChange method [Text Services Framework],ITextStoreAnchorSink interface, _tsf_itextstoreanchorsink_onselectionchange_ref, textstor/ITextStoreAnchorSink::OnSelectionChange, tsf.itextstoreanchorsink_onselectionchange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- textstor.h
: 
- ITextStoreAnchorSink.OnSelectionChange
: 
---

# ITextStoreAnchorSink::OnSelectionChange


## -description


The <b>ITextStoreAnchorSink::OnSelectionChange</b> method is called when the selection within the text stream changes. This method should be called whenever the return value of a potential call to <a href="https://msdn.microsoft.com/df1b21b7-b539-4546-96be-243a8e7ea75a">ITextStoreAnchor::GetSelection</a> has changed.


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



This method only needs to be called when the application modifies the selection itself, not when a client modifies the selection with <a href="https://msdn.microsoft.com/ce301fa4-d1dd-4470-b8b5-fc944afdc621">ITextStoreAnchor::SetSelection</a>, <a href="https://msdn.microsoft.com/f5cb512a-d9f5-451f-b6cb-2020ba32e855">ITextStoreAnchor::InsertTextAtSelection</a>, or other <a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a> methods.

When calling this method, the application must be able to grant a <a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">document lock</a>.

Applications should expect reentrant client calls to <a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock</a> from within this method. An application can grant the lock request synchronously, or, because several changes have been cached, it can grant the lock asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/3c623c44-b0d3-4b03-8de9-25f1062b5726">Document Locks</a>



<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor
      </a>



<a href="https://msdn.microsoft.com/f5cb512a-d9f5-451f-b6cb-2020ba32e855">ITextStoreAnchor::InsertTextAtSelection
      </a>



<a href="https://msdn.microsoft.com/ce301fa4-d1dd-4470-b8b5-fc944afdc621">ITextStoreAnchor::SetSelection
      </a>



<a href="https://msdn.microsoft.com/fb96b4fb-864f-4f32-bf7c-cf7f199e552a">ITextStoreAnchorSink</a>
 

 

