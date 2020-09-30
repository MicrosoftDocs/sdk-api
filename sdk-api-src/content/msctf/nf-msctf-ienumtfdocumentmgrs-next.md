---
UID: NF:msctf.IEnumTfDocumentMgrs.Next
title: IEnumTfDocumentMgrs::Next (msctf.h)
description: IEnumTfDocumentMgrs::Next method
helpviewer_keywords: ["IEnumTfDocumentMgrs interface [Text Services Framework]","Next method","IEnumTfDocumentMgrs.Next","IEnumTfDocumentMgrs::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfDocumentMgrs interface","_tsf_ienumtfdocumentmgrs_next_ref","msctf/IEnumTfDocumentMgrs::Next","tsf.ienumtfdocumentmgrs_next"]
old-location: tsf\ienumtfdocumentmgrs_next.htm
tech.root: TSF
ms.assetid: 2fe1beed-9952-4e6c-9c45-eb21c4918288
ms.date: 12/05/2018
ms.keywords: IEnumTfDocumentMgrs interface [Text Services Framework],Next method, IEnumTfDocumentMgrs.Next, IEnumTfDocumentMgrs::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfDocumentMgrs interface, _tsf_ienumtfdocumentmgrs_next_ref, msctf/IEnumTfDocumentMgrs::Next, tsf.ienumtfdocumentmgrs_next
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
 - IEnumTfDocumentMgrs::Next
 - msctf/IEnumTfDocumentMgrs::Next
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
 - IEnumTfDocumentMgrs.Next
---

# IEnumTfDocumentMgrs::Next


## -description

Obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param rgDocumentMgr [out]

Pointer to an array of <a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements were obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rgDocumentMgr</i> is invalid.

</td>
</tr>
</table>

## -see-also

[IEnumTfDocumentMgrs interface](nn-msctf-ienumtfdocumentmgrs.md), [ITfDocumentMgr interface](nn-msctf-itfdocumentmgr.md)