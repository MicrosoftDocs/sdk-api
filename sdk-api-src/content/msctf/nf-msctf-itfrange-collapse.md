---
UID: NF:msctf.ITfRange.Collapse
title: ITfRange::Collapse (msctf.h)
description: The ITfRange::Collapse method clears the range of text by moving its start anchor and end anchor to the same position.
helpviewer_keywords: ["Collapse","Collapse method [Text Services Framework]","Collapse method [Text Services Framework]","ITfRange interface","ITfRange interface [Text Services Framework]","Collapse method","ITfRange.Collapse","ITfRange::Collapse","TF_ANCHOR_END","TF_ANCHOR_START","_tsf_itfrange_collapse_ref","msctf/ITfRange::Collapse","tsf.itfrange_collapse"]
old-location: tsf\itfrange_collapse.htm
tech.root: TSF
ms.assetid: 657b1ffe-a958-4eb0-8014-6c068711b809
ms.date: 12/05/2018
ms.keywords: Collapse, Collapse method [Text Services Framework], Collapse method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],Collapse method, ITfRange.Collapse, ITfRange::Collapse, TF_ANCHOR_END, TF_ANCHOR_START, _tsf_itfrange_collapse_ref, msctf/ITfRange::Collapse, tsf.itfrange_collapse
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
 - ITfRange::Collapse
 - msctf/ITfRange::Collapse
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
 - ITfRange.Collapse
---

# ITfRange::Collapse


## -description

The <b>ITfRange::Collapse</b> method clears the range of text by moving its start anchor and end anchor to the same position.

## -parameters

### -param ec [in]

Edit cookie obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param aPos [in]

<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor
            </a> enumeration that describes how to collapse the range.

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
The end anchor is moved to the location of the start anchor.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_ANCHOR_END"></a><a id="tf_anchor_end"></a><dl>
<dt><b>TF_ANCHOR_END</b></dt>
</dl>
</td>
<td width="60%">
The start anchor is moved to the location of the end anchor.

</td>
</tr>
</table>

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
The object does not support the interface, or a new range cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>aPos</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The cookie in <i>ec</i> is invalid, or the caller does not have a read-only lock.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/TSF/text-stores">Text Stores</a>



<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor
      </a>