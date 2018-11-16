---
UID: NF:ctffunc.ITfCandidateList.GetCandidate
title: ITfCandidateList::GetCandidate
author: windows-sdk-content
description: ITfCandidateList::GetCandidate method
old-location: tsf\itfcandidatelist_getcandidate.htm
tech.root: TSF
ms.assetid: 4cb2127c-cce5-4815-b40b-e6e15058eab5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetCandidate, GetCandidate method [Text Services Framework], GetCandidate method [Text Services Framework],ITfCandidateList interface, ITfCandidateList interface [Text Services Framework],GetCandidate method, ITfCandidateList.GetCandidate, ITfCandidateList::GetCandidate, _tsf_itfcandidatelist_getcandidate_ref, ctffunc/ITfCandidateList::GetCandidate, tsf.itfcandidatelist_getcandidate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tiptsf.dll
api_name:
 - ITfCandidateList.GetCandidate
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- ctffunc.h
: 
- ITfCandidateList.GetCandidate
: 
---

# ITfCandidateList::GetCandidate


## -description




## -parameters




### -param nIndex [in]

Specifies the zero-based index of the candidate string to obtain.


### -param ppCand [out]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms538497(v=VS.85).aspx">ITfCandidateString</a> interface pointer that receives the candidate string object. The caller must release this interface when it is no longer required.


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
<i>nIndex</i> is invalid.

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




<a href="https://msdn.microsoft.com/en-us/library/ms538492(v=VS.85).aspx">ITfCandidateList</a>



<a href="https://msdn.microsoft.com/82c77b59-a50c-42ae-ba1d-25a1c196662d">ITfCandidateString
      </a>
 

 

