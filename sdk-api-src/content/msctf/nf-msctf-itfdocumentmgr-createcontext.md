---
UID: NF:msctf.ITfDocumentMgr.CreateContext
title: ITfDocumentMgr::CreateContext (msctf.h)
description: ITfDocumentMgr::CreateContext method
helpviewer_keywords: ["CreateContext","CreateContext method [Text Services Framework]","CreateContext method [Text Services Framework]","ITfDocumentMgr interface","ITfDocumentMgr interface [Text Services Framework]","CreateContext method","ITfDocumentMgr.CreateContext","ITfDocumentMgr::CreateContext","_tsf_itfdocumentmgr_createcontext_ref","msctf/ITfDocumentMgr::CreateContext","tsf.itfdocumentmgr_createcontext"]
old-location: tsf\itfdocumentmgr_createcontext.htm
tech.root: TSF
ms.assetid: 1415f338-731c-44c5-b798-edf823174272
ms.date: 12/05/2018
ms.keywords: CreateContext, CreateContext method [Text Services Framework], CreateContext method [Text Services Framework],ITfDocumentMgr interface, ITfDocumentMgr interface [Text Services Framework],CreateContext method, ITfDocumentMgr.CreateContext, ITfDocumentMgr::CreateContext, _tsf_itfdocumentmgr_createcontext_ref, msctf/ITfDocumentMgr::CreateContext, tsf.itfdocumentmgr_createcontext
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
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfDocumentMgr::CreateContext
 - msctf/ITfDocumentMgr::CreateContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfDocumentMgr.CreateContext
---

# ITfDocumentMgr::CreateContext


## -description

Creates a context object.

## -parameters

### -param tidOwner [in]

The client identifier. For an application, this value is provided by a previous call to <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate</a>. For a text service, this value is provided in the text service <a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate</a> method.

### -param dwFlags [in]

Reserved, must be zero.

### -param punk [in]

Pointer to an object that supports the <a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a> or <a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink">ITfContextOwnerCompositionSink</a> interfaces. This value can be <b>NULL</b>.

### -param ppic [out]

Address of an <a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> pointer that receives the context.

### -param pecTextStore [out]

Pointer to a <a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie</a> value that receives an edit cookie for the new context. This value identifies the context in various methods.

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

All references to the <i>punk</i> parameter are released when the context is destroyed or when the context is removed from the stack with the <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop</a> method.

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownercompositionsink">ITfContextOwnerCompositionSink
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate">ITfTextInputProcessor::Activate
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-activate">ITfThreadMgr::Activate
      </a>



<a href="/windows/desktop/TSF/tfeditcookie">TfEditCookie
      </a>