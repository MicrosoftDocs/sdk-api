---
UID: NF:msctf.ITfEditRecord.GetSelectionStatus
title: ITfEditRecord::GetSelectionStatus (msctf.h)
description: ITfEditRecord::GetSelectionStatus method
helpviewer_keywords: ["GetSelectionStatus","GetSelectionStatus method [Text Services Framework]","GetSelectionStatus method [Text Services Framework]","ITfEditRecord interface","ITfEditRecord interface [Text Services Framework]","GetSelectionStatus method","ITfEditRecord.GetSelectionStatus","ITfEditRecord::GetSelectionStatus","_tsf_itfeditrecord_getselectionstatus_ref","msctf/ITfEditRecord::GetSelectionStatus","tsf.itfeditrecord_getselectionstatus"]
old-location: tsf\itfeditrecord_getselectionstatus.htm
tech.root: TSF
ms.assetid: ad7dbd71-6241-45a0-9815-1f0eedc5213a
ms.date: 12/05/2018
ms.keywords: GetSelectionStatus, GetSelectionStatus method [Text Services Framework], GetSelectionStatus method [Text Services Framework],ITfEditRecord interface, ITfEditRecord interface [Text Services Framework],GetSelectionStatus method, ITfEditRecord.GetSelectionStatus, ITfEditRecord::GetSelectionStatus, _tsf_itfeditrecord_getselectionstatus_ref, msctf/ITfEditRecord::GetSelectionStatus, tsf.itfeditrecord_getselectionstatus
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
 - ITfEditRecord::GetSelectionStatus
 - msctf/ITfEditRecord::GetSelectionStatus
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
 - ITfEditRecord.GetSelectionStatus
---

# ITfEditRecord::GetSelectionStatus


## -description

Determines if the selection has changed during the edit session.

## -parameters

### -param pfChanged [out]

Pointer to a <b>BOOL</b> value that receives a value that indicates if the selection changed due to an edit session. Receives a nonzero value if the selection changed or zero otherwise.

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
<i>pfChanged</i> is invalid.

</td>
</tr>
</table>

