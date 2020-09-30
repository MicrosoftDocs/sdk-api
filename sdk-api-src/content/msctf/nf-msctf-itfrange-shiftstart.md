---
UID: NF:msctf.ITfRange.ShiftStart
title: ITfRange::ShiftStart (msctf.h)
description: ITfRange::ShiftStart method
helpviewer_keywords: ["ITfRange interface [Text Services Framework]","ShiftStart method","ITfRange.ShiftStart","ITfRange::ShiftStart","ShiftStart","ShiftStart method [Text Services Framework]","ShiftStart method [Text Services Framework]","ITfRange interface","_tsf_itfrange_shiftstart_ref","msctf/ITfRange::ShiftStart","tsf.itfrange_shiftstart"]
old-location: tsf\itfrange_shiftstart.htm
tech.root: TSF
ms.assetid: f9f983b1-a5fa-4857-b73c-b879c566d6f6
ms.date: 12/05/2018
ms.keywords: ITfRange interface [Text Services Framework],ShiftStart method, ITfRange.ShiftStart, ITfRange::ShiftStart, ShiftStart, ShiftStart method [Text Services Framework], ShiftStart method [Text Services Framework],ITfRange interface, _tsf_itfrange_shiftstart_ref, msctf/ITfRange::ShiftStart, tsf.itfrange_shiftstart
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
 - ITfRange::ShiftStart
 - msctf/ITfRange::ShiftStart
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
 - ITfRange.ShiftStart
---

# ITfRange::ShiftStart


## -description

Moves the start anchor of the range.

## -parameters

### -param ec [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext</a> or <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param cchReq [in]

Contains the number of characters the start anchor is shifted. A negative value causes the anchor to move backward and a positive value causes the anchor to move forward.

### -param pcch [out]

Pointer to a <b>LONG</b> value that receives the number of characters the anchor was shifted.

### -param pHalt [in]

Pointer to a <a href="/windows/desktop/api/msctf/ns-msctf-tf_haltcond">TF_HALTCOND</a> structure that contains conditions about the shift. This parameter is optional and can be <b>NULL</b>.

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

This method cannot move an anchor beyond a region boundary. If the shift reaches a region boundary, the number of characters actually shifted will be less than requested. <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstartregion">ITfRange::ShiftStartRegion</a> is used to shift the anchor to an adjacent region.

If the shift operation causes the range start anchor to move past the end anchor, the end anchor is moved to the same location as the start anchor.

<b>ITfRange::ShiftStart</b> can be a lengthy operation. For better performance, use <a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstarttorange">ITfRange::ShiftStartToRange</a> when possible.

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfdocumentmgr-createcontext">ITfDocumentMgr::CreateContext
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftend">ITfRange::ShiftEnd
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstartregion">ITfRange::ShiftStartRegion
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfrange-shiftstarttorange">ITfRange::ShiftStartToRange
      </a>



<a href="/windows/desktop/api/msctf/ns-msctf-tf_haltcond">TF_HALTCOND
      </a>