---
UID: NF:msctf.ITfRange.IsEqualEnd
title: ITfRange::IsEqualEnd (msctf.h)
description: The ITfRange::IsEqualStart method verifies that the end anchor of this range of text matches an anchor of another specified range.
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","IsEqualEnd method","ITfRange.IsEqualEnd","ITfRange::IsEqualEnd","IsEqualEnd","IsEqualEnd method [Text Services Framework]","IsEqualEnd method [Text Services Framework]","ITfRange interface","TF_ANCHOR_END","TF_ANCHOR_START","_tsf_itfrange_isequalend_ref","msctf/ITfRange::IsEqualEnd","tsf.itfrange_isequalend"]
old-location: tsf\itfrange_isequalend.htm
tech.root: TSF
ms.assetid: 03b87230-457f-4483-a183-d8a8cc7cead4
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],IsEqualEnd method, ITfRange.IsEqualEnd, ITfRange::IsEqualEnd, IsEqualEnd, IsEqualEnd method [Text Services Framework], IsEqualEnd method [Text Services Framework],ITfRange interface, TF_ANCHOR_END, TF_ANCHOR_START, _tsf_itfrange_isequalend_ref, msctf/ITfRange::IsEqualEnd, tsf.itfrange_isequalend
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
 - ITfRange::IsEqualEnd
 - msctf/ITfRange::IsEqualEnd
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
 - ITfRange.IsEqualEnd
---

# ITfRange::IsEqualEnd


## -description

The <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-isequalstart">ITfRange::IsEqualStart</a> method verifies that the end anchor of this range of text matches an anchor of another specified range.

## -parameters

### -param ec [in]

Edit cookie obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pWith [in]

Pointer to a specified range in which an anchor is to be compared to this range end anchor.

### -param aPos [in]

Enumeration element that indicates which anchor of the specified <i>pWith</i> range to compare with this range end anchor.

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
Compares this range end anchor with the specified range start anchor.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_END"></a><a id="tf_anchor_end"></a><dl>
<dt><b>TF_ANCHOR_END</b></dt>
</dl>
</td>
<td width="60%">
Compares this range end anchor with the specified range end anchor.

</td>
</tr>
</table>

### -param pfEqual [out]

Pointer to a Boolean value. Upon return, <b>TRUE</b> indicates that the specified <i>pWith</i> range anchor matches this range end anchor. <b>FALSE</b> indicates otherwise.

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

This method is identical to <b>ITfRange::IsEqualStart</b>, except that the end anchor of this range is compared to an anchor of another specified range.

This method is functionally equivalent to, but more efficient than, <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-compareend">ITfRange::CompareEnd</a>.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-compareend">ITfRange::CompareEnd
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-isequalstart">ITfRange:IsEqualStart
      </a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>



<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor
      </a>