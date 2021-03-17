---
UID: NF:ctffunc.IEnumTfCandidates.Skip
title: IEnumTfCandidates::Skip (ctffunc.h)
description: IEnumTfCandidates::Skip method
helpviewer_keywords: ["IEnumTfCandidates interface [Text Services Framework]","Skip method","IEnumTfCandidates.Skip","IEnumTfCandidates::Skip","Skip","Skip method [Text Services Framework]","Skip method [Text Services Framework]","IEnumTfCandidates interface","_tsf_ienumtfcandidates_skip_ref","ctffunc/IEnumTfCandidates::Skip","tsf.ienumtfcandidates_skip"]
old-location: tsf\ienumtfcandidates_skip.htm
tech.root: TSF
ms.assetid: f32587f2-cdfa-4cbc-8a5c-f6630c7866f9
ms.date: 12/05/2018
ms.keywords: IEnumTfCandidates interface [Text Services Framework],Skip method, IEnumTfCandidates.Skip, IEnumTfCandidates::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfCandidates interface, _tsf_ienumtfcandidates_skip_ref, ctffunc/IEnumTfCandidates::Skip, tsf.ienumtfcandidates_skip
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
 - IEnumTfCandidates::Skip
 - ctffunc/IEnumTfCandidates::Skip
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
 - IEnumTfCandidates.Skip
---

# IEnumTfCandidates::Skip


## -description

Moves the current position forward in the enumeration sequence by the specified number of elements.

## -parameters

### -param ulCount [in]

Contains the number of elements to skip.

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
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>

