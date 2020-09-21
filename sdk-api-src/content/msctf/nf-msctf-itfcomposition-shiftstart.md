---
UID: NF:msctf.ITfComposition.ShiftStart
title: ITfComposition::ShiftStart (msctf.h)
description: ITfComposition::ShiftStart method
helpviewer_keywords: ["ITfComposition interface [Text Services Framework]","ShiftStart method","ITfComposition.ShiftStart","ITfComposition::ShiftStart","ShiftStart","ShiftStart method [Text Services Framework]","ShiftStart method [Text Services Framework]","ITfComposition interface","_tsf_itfcomposition_shiftstart_ref","msctf/ITfComposition::ShiftStart","tsf.itfcomposition_shiftstart"]
old-location: tsf\itfcomposition_shiftstart.htm
tech.root: TSF
ms.assetid: 85a5121a-7be0-4703-a1d4-4de21dd98697
ms.date: 12/05/2018
ms.keywords: ITfComposition interface [Text Services Framework],ShiftStart method, ITfComposition.ShiftStart, ITfComposition::ShiftStart, ShiftStart, ShiftStart method [Text Services Framework], ShiftStart method [Text Services Framework],ITfComposition interface, _tsf_itfcomposition_shiftstart_ref, msctf/ITfComposition::ShiftStart, tsf.itfcomposition_shiftstart
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
 - ITfComposition::ShiftStart
 - msctf/ITfComposition::ShiftStart
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
 - ITfComposition.ShiftStart
---

# ITfComposition::ShiftStart


## -description

Moves the start anchor of a composition.

## -parameters

### -param ecWrite [in]

Contains an edit cookie that identifies the edit context obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pNewStart [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that contains the new start anchor position. The start anchor of the context will be moved to the start anchor of this range. This method fails if the start anchor of this range is positioned beyond the end anchor of the composition.

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
The start anchor of <i>pNewStart</i> is positioned past the end anchor of the composition or <i>pNewStart</i> is invalid.

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

This method causes the GUID_PROP_COMPOSING property to be removed from any text removed from the composition. Likewise, the GUID_PROP_COMPOSING property will also be added to any text added to the composition.

## -see-also

[ITfComposition interface](nn-msctf-itfcomposition.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md), [ITfRange interface](nn-msctf-itfrange.md), [ITfComposition::ShiftEnd](nf-msctf-itfcomposition-shiftend.md)