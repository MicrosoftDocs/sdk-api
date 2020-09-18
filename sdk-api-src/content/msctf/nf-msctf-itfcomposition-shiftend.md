---
UID: NF:msctf.ITfComposition.ShiftEnd
title: ITfComposition::ShiftEnd (msctf.h)
description: ITfComposition::ShiftEnd method
helpviewer_keywords: ["ITfComposition interface [Text Services Framework]","ShiftEnd method","ITfComposition.ShiftEnd","ITfComposition::ShiftEnd","ShiftEnd","ShiftEnd method [Text Services Framework]","ShiftEnd method [Text Services Framework]","ITfComposition interface","_tsf_itfcomposition_shiftend_ref","msctf/ITfComposition::ShiftEnd","tsf.itfcomposition_shiftend"]
old-location: tsf\itfcomposition_shiftend.htm
tech.root: TSF
ms.assetid: 40472318-85de-4cff-ac60-adfcbacc1537
ms.date: 12/05/2018
ms.keywords: ITfComposition interface [Text Services Framework],ShiftEnd method, ITfComposition.ShiftEnd, ITfComposition::ShiftEnd, ShiftEnd, ShiftEnd method [Text Services Framework], ShiftEnd method [Text Services Framework],ITfComposition interface, _tsf_itfcomposition_shiftend_ref, msctf/ITfComposition::ShiftEnd, tsf.itfcomposition_shiftend
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
 - ITfComposition::ShiftEnd
 - msctf/ITfComposition::ShiftEnd
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
 - ITfComposition.ShiftEnd
---

# ITfComposition::ShiftEnd


## -description

Moves the end anchor of a composition.

## -parameters

### -param ecWrite [in]

Contains an edit cookie that identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pNewEnd [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that contains the new end anchor position. The end anchor of the context will be moved to the end anchor of this range. This method fails if the end anchor of this range is positioned prior to the start anchor of the composition.

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
The end anchor of <i>pNewEnd</i> is positioned prior to the start anchor of the composition or <i>pNewStart</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The composition has already terminated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ecWrite</i> does not have a read/write lock.

</td>
</tr>
</table>

## -remarks

This method causes the GUID_PROP_COMPOSING property to be removed from any text removed from the composition. Likewise, the GUID_PROP_COMPOSING property is also added to any text added to the composition.

## -see-also

[ITfComposition interface](nn-msctf-itfcomposition.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md), [ITfRange interface](nn-msctf-itfrange.md), [ITfComposition::ShiftStart](nf-msctf-itfcomposition-shiftstart.md)