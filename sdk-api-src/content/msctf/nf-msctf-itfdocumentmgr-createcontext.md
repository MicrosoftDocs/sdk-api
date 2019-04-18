---
UID: NF:msctf.ITfDocumentMgr.CreateContext
title: ITfDocumentMgr::CreateContext (msctf.h)
author: windows-sdk-content
description: ITfDocumentMgr::CreateContext method
old-location: tsf\itfdocumentmgr_createcontext.htm
tech.root: TSF
ms.assetid: 1415f338-731c-44c5-b798-edf823174272
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateContext, CreateContext method [Text Services Framework], CreateContext method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],CreateContext method, ITfDocumentMgr.CreateContext, ITfDocumentMgr::CreateContext, _tsf_itfdocumentmgr_createcontext_ref, msctf/ITfDocumentMgr::CreateContext, tsf.itfdocumentmgr_createcontext
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfDocumentMgr.CreateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfDocumentMgr::CreateContext


## -description




## -parameters




### -param tidOwner [in]

The client identifier. For an application, this value is provided by a previous call to <a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate</a>. For a text service, this value is provided in the text service <a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate</a> method.


### -param dwFlags [in]

Reserved, must be zero.


### -param punk [in]

Pointer to an object that supports the <a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a> or <a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink</a> interfaces. This value can be <b>NULL</b>.


### -param ppic [out]

Address of an <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> pointer that receives the context.


### -param pecTextStore [out]

Pointer to a <a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie</a> value that receives an edit cookie for the new context. This value identifies the context in various methods.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation error occurred.

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
</table>
 




## -remarks



All references to the <i>punk</i> parameter are released when the context is destroyed or when the context is removed from the stack with the <a href="https://msdn.microsoft.com/bbf65d8d-5a59-4c4b-a132-fa28babcd70b">ITfDocumentMgr::Pop</a> method.




## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP
      </a>



<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink
      </a>



<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a>



<a href="https://msdn.microsoft.com/bbf65d8d-5a59-4c4b-a132-fa28babcd70b">ITfDocumentMgr::Pop
      </a>



<a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate
      </a>



<a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">ITfThreadMgr::Activate
      </a>



<a href="https://msdn.microsoft.com/1de17286-5d56-4302-a144-5fe6ca7d5557">TfEditCookie
      </a>
 

 

