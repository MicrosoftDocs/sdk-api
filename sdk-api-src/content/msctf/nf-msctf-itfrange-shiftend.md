---
UID: NF:msctf.ITfRange.ShiftEnd
title: ITfRange::ShiftEnd (msctf.h)
description: ITfRange::ShiftEnd method
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","ShiftEnd method","ITfRange.ShiftEnd","ITfRange::ShiftEnd","ShiftEnd","ShiftEnd method [Text Services Framework]","ShiftEnd method [Text Services Framework]","ITfRange interface","_tsf_itfrange_shiftend_ref","msctf/ITfRange::ShiftEnd","tsf.itfrange_shiftend"]
old-location: tsf\itfrange_shiftend.htm
tech.root: TSF
ms.assetid: 1debec6d-f98f-45a4-aaa8-99b61f3583ef
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftEnd method, ITfRange.ShiftEnd, ITfRange::ShiftEnd, ShiftEnd, ShiftEnd method [Text Services Framework], ShiftEnd method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftend_ref, msctf/ITfRange::ShiftEnd, tsf.itfrange_shiftend
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
 - ITfRange::ShiftEnd
 - msctf/ITfRange::ShiftEnd
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
 - ITfRange.ShiftEnd
---

# ITfRange::ShiftEnd


## -description

Moves the end anchor of the range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param cchReq [in]

Contains the number of characters that the end anchor is shifted. A negative value causes the anchor to move backward and a positive value causes the anchor to move forward.

### -param pcch [out]

Pointer to a <b>LONG</b> value that receives the number of characters the anchor shifted.

### -param pHalt [in]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_haltcond">TF_HALTCOND</a> structure that contains conditions on the shift. This parameter is optional and can be <b>NULL</b>.

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
The edit context identified by <i>ec</i> does not have a read-only lock.

</td>
</tr>
</table>

## -remarks

The start and end positions of a range are called anchors.

This method cannot move an anchor beyond a region boundary. If the shift reaches a region boundary, the number of characters actually shifted will be less than requested. <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendregion">ITfRange::ShiftEndRegion</a> is used to shift the anchor to an adjacent region.

If the shift operation causes the range end anchor to move past the start anchor, the start anchor is moved to the same location as the end anchor.

ITfRange::ShiftEnd can be a lengthy operation. For better performance, use <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstarttorange">ITfRange::ShiftEndToRange</a> when possible.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftendregion">ITfRange::ShiftEndRegion
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstart">ITfRange::ShiftStart
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_haltcond">TF_HALTCOND
      </a>