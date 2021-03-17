---
UID: NF:msctf.ITfRange.ShiftStartToRange
title: ITfRange::ShiftStartToRange (msctf.h)
description: ITfRange::ShiftStartToRange method
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","ShiftStartToRange method","ITfRange.ShiftStartToRange","ITfRange::ShiftStartToRange","ShiftStartToRange","ShiftStartToRange method [Text Services Framework]","ShiftStartToRange method [Text Services Framework]","ITfRange interface","_tsf_itfrange_shiftstarttorange_ref","msctf/ITfRange::ShiftStartToRange","tsf.itfrange_shiftstarttorange"]
old-location: tsf\itfrange_shiftstarttorange.htm
tech.root: TSF
ms.assetid: 8e3e40a0-71ba-4abf-ac99-99d66856746c
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftStartToRange method, ITfRange.ShiftStartToRange, ITfRange::ShiftStartToRange, ShiftStartToRange, ShiftStartToRange method [Text Services Framework], ShiftStartToRange method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftstarttorange_ref, msctf/ITfRange::ShiftStartToRange, tsf.itfrange_shiftstarttorange
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
 - ITfRange::ShiftStartToRange
 - msctf/ITfRange::ShiftStartToRange
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
 - ITfRange.ShiftStartToRange
---

# ITfRange::ShiftStartToRange


## -description

Moves the start anchor of this range to an anchor within another range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that contains the anchor that the start anchor is moved to.

### -param aPos [in]

Contains one of the <a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor</a> values that specifies which anchor of <i>pRange</i> the start anchor is moved to.

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
<i>pRange</i> is invalid.

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
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ec</i> does not have a read-only lock.

</td>
</tr>
</table>

## -remarks

The start and end positions of a range are called anchors.

If the shift operation causes the range start anchor to move past the end anchor, the end anchor is moved to the same location as the start anchor.

This method is more efficient than <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstart">ITfRange::ShiftStart</a> and should be used when possible.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendtorange">ITfRange::ShiftEndToRange
      </a>



ITfRange::ShiftStart



<a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor
      </a>