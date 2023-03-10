---
UID: NF:msctf.ITfRange.GetText
title: ITfRange::GetText (msctf.h)
description: The ITfRange::GetText method obtains the content covered by this range of text.
helpviewer_keywords: ["GetText","GetText method [Text Services Framework]","GetText method [Text Services Framework]","ITfRange interface","ITfRange interface [Text Services Framework]","GetText method","ITfRange.GetText","ITfRange::GetText","TF_TF_IGNOREEND","TF_TF_MOVESTART","_tsf_itfrange_gettext_ref","msctf/ITfRange::GetText","tsf.itfrange_gettext"]
old-location: tsf\itfrange_gettext.htm
tech.root: TSF
ms.assetid: b38a8de3-947f-469c-9f0d-f0482ea86884
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Text Services Framework], GetText method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetText method, ITfRange.GetText, ITfRange::GetText, TF_TF_IGNOREEND, TF_TF_MOVESTART, _tsf_itfrange_gettext_ref, msctf/ITfRange::GetText, tsf.itfrange_gettext
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
 - ITfRange::GetText
 - msctf/ITfRange::GetText
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
 - ITfRange.GetText
---

# ITfRange::GetText


## -description

The <b>ITfRange::GetText</b> method obtains the content covered by this range of text.

## -parameters

### -param ec [in]

Edit cookie that identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param dwFlags [in]

Bit fields that specify optional behavior.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_TF_MOVESTART"></a><a id="tf_tf_movestart"></a><dl>
<dt><b>TF_TF_MOVESTART</b></dt>
</dl>
</td>
<td width="60%">
Start anchor of the range is advanced to the position after the last character returned.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_TF_IGNOREEND"></a><a id="tf_tf_ignoreend"></a><dl>
<dt><b>TF_TF_IGNOREEND</b></dt>
</dl>
</td>
<td width="60%">
Method attempts to fill <i>pchText</i> with the maximum number of characters, instead of halting the copy at the position occupied by the end anchor of the range.

</td>
</tr>
</table>

### -param pchText [out]

Pointer to a buffer to receive the text in the range.

### -param cchMax [in]

Maximum size of the text buffer.

### -param pcch [out]

Pointer to a ULONG representing the number of characters written to the <i>pchText</i> text buffer.

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
The value of the <i>ec</i> parameter is an invalid cookie, or the caller does not have a read-only lock.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/TSF/tf-tf--constants">TF_TF_* Constants</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>