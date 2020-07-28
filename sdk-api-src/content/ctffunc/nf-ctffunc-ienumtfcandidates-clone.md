---
UID: NF:ctffunc.IEnumTfCandidates.Clone
title: IEnumTfCandidates::Clone (ctffunc.h)
description: IEnumTfCandidates::Clone method
helpviewer_keywords: ["Clone","Clone method [Text Services Framework]","Clone method [Text Services Framework]","IEnumTfCandidates interface","IEnumTfCandidates interface [Text Services Framework]","Clone method","IEnumTfCandidates.Clone","IEnumTfCandidates::Clone","_tsf_ienumtfcandidates_clone_ref","ctffunc/IEnumTfCandidates::Clone","tsf.ienumtfcandidates_clone"]
old-location: tsf\ienumtfcandidates_clone.htm
tech.root: TSF
ms.assetid: 7e7fc6d9-69eb-4457-be28-2b28b9eeeabb
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfCandidates interface, IEnumTfCandidates interface [Text Services Framework],Clone method, IEnumTfCandidates.Clone, IEnumTfCandidates::Clone, _tsf_ienumtfcandidates_clone_ref, ctffunc/IEnumTfCandidates::Clone, tsf.ienumtfcandidates_clone
f1_keywords:
- ctffunc/IEnumTfCandidates.Clone
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.dll
api_name:
- IEnumTfCandidates.Clone
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# IEnumTfCandidates::Clone


## -description

Creates a copy of the enumerator object.

## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-ienumtfcandidates">IEnumTfCandidates</a> interface pointer that receives the new enumerator.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ctffunc/nn-ctffunc-ienumtfcandidates">IEnumTfCandidates
      </a>
 

 

