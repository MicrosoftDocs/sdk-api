---
UID: NF:msctf.ITfRange.ShiftEndToRange
title: ITfRange::ShiftEndToRange (msctf.h)
description: ITfRange::ShiftEndToRange method
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","ShiftEndToRange method","ITfRange.ShiftEndToRange","ITfRange::ShiftEndToRange","ShiftEndToRange","ShiftEndToRange method [Text Services Framework]","ShiftEndToRange method [Text Services Framework]","ITfRange interface","_tsf_itfrange_shiftendtorange_ref","msctf/ITfRange::ShiftEndToRange","tsf.itfrange_shiftendtorange"]
old-location: tsf\itfrange_shiftendtorange.htm
tech.root: TSF
ms.assetid: 27595909-025b-46c9-bd6f-2e64a720c97c
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftEndToRange method, ITfRange.ShiftEndToRange, ITfRange::ShiftEndToRange, ShiftEndToRange, ShiftEndToRange method [Text Services Framework], ShiftEndToRange method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftendtorange_ref, msctf/ITfRange::ShiftEndToRange, tsf.itfrange_shiftendtorange
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
 - ITfRange::ShiftEndToRange
 - msctf/ITfRange::ShiftEndToRange
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
 - ITfRange.ShiftEndToRange
---

# ITfRange::ShiftEndToRange


## -description

Moves the end anchor of this range to an anchor within another range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> interface that contains the anchor that the end anchor is moved to.

### -param aPos [in]

Contains one of the <a href="/windows/win32/api/msctf/ne-msctf-tfanchor">TfAnchor</a> values that specify which anchor of <i>pRange</i> the end anchor will get moved to.

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

If the shift operation causes the range end anchor to move past the start anchor, the start anchor is moved to the same location as the end anchor.

This method is more efficient than <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftend">ITfRange::ShiftEnd</a> and should be used.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftend">ITfRange::ShiftEnd
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstarttorange">ITfRange::ShiftStartToRange
      </a>