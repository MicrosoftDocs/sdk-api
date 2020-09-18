---
UID: NF:msctf.ITfContext.GetDocumentMgr
title: ITfContext::GetDocumentMgr (msctf.h)
description: ITfContext::GetDocumentMgr method
helpviewer_keywords: ["GetDocumentMgr","GetDocumentMgr method [Text Services Framework]","GetDocumentMgr method [Text Services Framework]","ITfContext interface","ITfContext interface [Text Services Framework]","GetDocumentMgr method","ITfContext.GetDocumentMgr","ITfContext::GetDocumentMgr","_tsf_itfcontext_getdocumentmgr_ref","msctf/ITfContext::GetDocumentMgr","tsf.itfcontext_getdocumentmgr"]
old-location: tsf\itfcontext_getdocumentmgr.htm
tech.root: TSF
ms.assetid: 21fa683d-c386-4aa2-8bc5-d5170443c5cd
ms.date: 12/05/2018
ms.keywords: GetDocumentMgr, GetDocumentMgr method [Text Services Framework], GetDocumentMgr method [Text Services Framework],ITfContext interface, ITfContext interface [Text Services Framework],GetDocumentMgr method, ITfContext.GetDocumentMgr, ITfContext::GetDocumentMgr, _tsf_itfcontext_getdocumentmgr_ref, msctf/ITfContext::GetDocumentMgr, tsf.itfcontext_getdocumentmgr
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
 - ITfContext::GetDocumentMgr
 - msctf/ITfContext::GetDocumentMgr
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
 - ITfContext.GetDocumentMgr
---

# ITfContext::GetDocumentMgr


## -description

Obtains the document manager that contains the context.

## -parameters

### -param ppDm [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface pointer that receives the document manager.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The context is not contained in any document manager. <i>ppDm</i> is set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppDm</i> is invalid.

</td>
</tr>
</table>

## -remarks

If the context is not contained within a document manager, this method returns S_FALSE and <i>ppDm</i> is set to <b>NULL</b>. This occurs when the context is removed from the context stack through a call to <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-pop">ITfDocumentMgr::Pop</a>.

## -see-also

[ITfContext interface](nn-msctf-itfcontext.md), [ITfDocumentMgr interface](nn-msctf-itfdocumentmgr.md), [ITfDocumentMgr::Pop](nf-msctf-itfdocumentmgr-pop.md)