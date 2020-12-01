---
UID: NF:ctffunc.IEnumTfCandidates.Next
title: IEnumTfCandidates::Next (ctffunc.h)
description: IEnumTfCandidates::Next method
helpviewer_keywords: ["IEnumTfCandidates interface [Text Services Framework]","Next method","IEnumTfCandidates.Next","IEnumTfCandidates::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfCandidates interface","_tsf_ienumtfcandidates_next_ref","ctffunc/IEnumTfCandidates::Next","tsf.ienumtfcandidates_next"]
old-location: tsf\ienumtfcandidates_next.htm
tech.root: TSF
ms.assetid: 50aaa3c0-6998-49de-9753-7be38625a10d
ms.date: 12/05/2018
ms.keywords: IEnumTfCandidates interface [Text Services Framework],Next method, IEnumTfCandidates.Next, IEnumTfCandidates::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfCandidates interface, _tsf_ienumtfcandidates_next_ref, ctffunc/IEnumTfCandidates::Next, tsf.ienumtfcandidates_next
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - IEnumTfCandidates::Next
 - ctffunc/IEnumTfCandidates::Next
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
 - IEnumTfCandidates.Next
---

# IEnumTfCandidates::Next


## -description

Obtains, from the current position, the specified number of elements in the enumeration sequence.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param ppCand [out]

Pointer to an array of <a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatestring">ITfCandidateString</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.

### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<i>ppCand</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-ienumtfcandidates">IEnumTfCandidates</a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itfcandidatestring">ITfCandidateString
      </a>