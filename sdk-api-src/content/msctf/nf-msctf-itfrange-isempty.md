---
UID: NF:msctf.ITfRange.IsEmpty
title: ITfRange::IsEmpty (msctf.h)
description: The ITfRange::IsEmpty method verifies that the range of text is empty because the start and end anchors occupy the same position.
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","IsEmpty method","ITfRange.IsEmpty","ITfRange::IsEmpty","IsEmpty","IsEmpty method [Text Services Framework]","IsEmpty method [Text Services Framework]","ITfRange interface","_tsf_itfrange_isempty_ref","msctf/ITfRange::IsEmpty","tsf.itfrange_isempty"]
old-location: tsf\itfrange_isempty.htm
tech.root: TSF
ms.assetid: 4cc720c1-acc1-445e-830e-91135fdfeeed
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],IsEmpty method, ITfRange.IsEmpty, ITfRange::IsEmpty, IsEmpty, IsEmpty method [Text Services Framework], IsEmpty method [Text Services Framework],ITfRange interface, _tsf_itfrange_isempty_ref, msctf/ITfRange::IsEmpty, tsf.itfrange_isempty
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
 - ITfRange::IsEmpty
 - msctf/ITfRange::IsEmpty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfRange.IsEmpty
---

# ITfRange::IsEmpty


## -description

The <b>ITfRange::IsEmpty</b> method verifies that the range of text is empty because the start and end anchors occupy the same position.

## -parameters

### -param ec [in]

Edit cookie that identifies the edit context. It is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pfEmpty [out]

Pointer to a Boolean value. <b>TRUE</b> indicates the range is empty; <b>FALSE</b> indicates the range is not empty.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The value of the <i>ec</i> parameter is an invalid cookie.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>