---
UID: NF:msctf.ITfRange.IsEqualStart
title: ITfRange::IsEqualStart (msctf.h)
description: The ITfRange::IsEqualStart method verifies that the start anchor of this range of text matches an anchor of another specified range.
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","IsEqualStart method","ITfRange.IsEqualStart","ITfRange::IsEqualStart","IsEqualStart","IsEqualStart method [Text Services Framework]","IsEqualStart method [Text Services Framework]","ITfRange interface","TF_ANCHOR_END","TF_ANCHOR_START","_tsf_itfrange_isequalstart_ref","msctf/ITfRange::IsEqualStart","tsf.itfrange_isequalstart"]
old-location: tsf\itfrange_isequalstart.htm
tech.root: TSF
ms.assetid: 562c2821-9522-4fb5-ae15-4430cd2711c6
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],IsEqualStart method, ITfRange.IsEqualStart, ITfRange::IsEqualStart, IsEqualStart, IsEqualStart method [Text Services Framework], IsEqualStart method [Text Services Framework],ITfRange interface, TF_ANCHOR_END, TF_ANCHOR_START, _tsf_itfrange_isequalstart_ref, msctf/ITfRange::IsEqualStart, tsf.itfrange_isequalstart
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
 - ITfRange::IsEqualStart
 - msctf/ITfRange::IsEqualStart
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
 - ITfRange.IsEqualStart
---

# ITfRange::IsEqualStart


## -description

The <b>ITfRange::IsEqualStart</b> method verifies that the start anchor of this range of text matches an anchor of another specified range.

## -parameters

### -param ec [in]

Edit cookie obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pWith [in]

Pointer to a specified range in which an anchor is to be compared to this range start anchor.

### -param aPos [in]

Enumeration element that indicates which anchor of the specified <i>pWith</i> range to compare to this range start anchor.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_START"></a><a id="tf_anchor_start"></a><dl>
<dt><b>TF_ANCHOR_START</b></dt>
</dl>
</td>
<td width="60%">
Compares this range start anchor with the specified range start anchor.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_END"></a><a id="tf_anchor_end"></a><dl>
<dt><b>TF_ANCHOR_END</b></dt>
</dl>
</td>
<td width="60%">
Compares this range start anchor with the specified range end anchor.

</td>
</tr>
</table>

### -param pfEqual [out]

Pointer to a Boolean value. Upon return, <b>TRUE</b> indicates that the specified <i>pWith</i> range anchor matches this range start anchor. <b>FALSE</b> indicates otherwise.

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

## -remarks

This method is identical to, but more efficient than, <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-comparestart">ITfRange::CompareStart</a>.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-comparestart">ITfRange::CompareStart
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-isequalend">ITfRange:IsEqualEnd
      </a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>



<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor
      </a>