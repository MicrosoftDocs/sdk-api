---
UID: NF:ctffunc.ITfCandidateList.GetCandidateNum
title: ITfCandidateList::GetCandidateNum (ctffunc.h)
description: ITfCandidateList::GetCandidateNum method
helpviewer_keywords: ["GetCandidateNum","GetCandidateNum method [Text Services Framework]","GetCandidateNum method [Text Services Framework]","ITfCandidateList interface","ITfCandidateList interface [Text Services Framework]","GetCandidateNum method","ITfCandidateList.GetCandidateNum","ITfCandidateList::GetCandidateNum","_tsf_itfcandidatelist_getcandidatenum_ref","ctffunc/ITfCandidateList::GetCandidateNum","tsf.itfcandidatelist_getcandidatenum"]
old-location: tsf\itfcandidatelist_getcandidatenum.htm
tech.root: TSF
ms.assetid: 53b8f8cc-776c-454a-86fa-6fa3b6ac097b
ms.date: 12/05/2018
ms.keywords: GetCandidateNum, GetCandidateNum method [Text Services Framework], GetCandidateNum method [Text Services Framework],ITfCandidateList interface, ITfCandidateList interface [Text Services Framework],GetCandidateNum method, ITfCandidateList.GetCandidateNum, ITfCandidateList::GetCandidateNum, _tsf_itfcandidatelist_getcandidatenum_ref, ctffunc/ITfCandidateList::GetCandidateNum, tsf.itfcandidatelist_getcandidatenum
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
req.dll: Tiptsf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfCandidateList::GetCandidateNum
 - ctffunc/ITfCandidateList::GetCandidateNum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tiptsf.dll
api_name:
 - ITfCandidateList.GetCandidateNum
---

# ITfCandidateList::GetCandidateNum


## -description

Obtains the number of candidate string objects in the candidate list.

## -parameters

### -param pnCnt [out]

Pointer to a <b>ULONG</b> value that receives the number of candidate string objects in the candidate list.

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
<i>pnCnt</i> is invalid.

</td>
</tr>
</table>

