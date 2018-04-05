---
UID: NF:ctffunc.ITfCandidateList.GetCandidateNum
title: ITfCandidateList::GetCandidateNum method
author: windows-driver-content
description: ITfCandidateList::GetCandidateNum method
old-location: tsf\itfcandidatelist_getcandidatenum.htm
old-project: TSF
ms.assetid: 53b8f8cc-776c-454a-86fa-6fa3b6ac097b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCandidateNum method [Text Services Framework], GetCandidateNum method [Text Services Framework], ITfCandidateList interface, GetCandidateNum,ITfCandidateList.GetCandidateNum, ITfCandidateList, ITfCandidateList interface [Text Services Framework], GetCandidateNum method, ITfCandidateList::GetCandidateNum, _tsf_itfcandidatelist_getcandidatenum_ref, ctffunc/ITfCandidateList::GetCandidateNum, tsf.itfcandidatelist_getcandidatenum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tiptsf.dll
api_name:
-	ITfCandidateList.GetCandidateNum
product: Windows
targetos: Windows
req.lib: 
req.dll: Tiptsf.dll
req.irql: 
---

# ITfCandidateList::GetCandidateNum method


## -description




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
 



