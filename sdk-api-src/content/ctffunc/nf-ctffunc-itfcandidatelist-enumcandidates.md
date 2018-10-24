---
UID: NF:ctffunc.ITfCandidateList.EnumCandidates
title: ITfCandidateList::EnumCandidates
author: windows-sdk-content
description: ITfCandidateList::EnumCandidates method
old-location: tsf\itfcandidatelist_enumcandidates.htm
tech.root: TSF
ms.assetid: f63799a1-2284-4da8-933c-f3616c1cb295
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: EnumCandidates, EnumCandidates method [Text Services Framework], EnumCandidates method [Text Services Framework],ITfCandidateList interface, ITfCandidateList interface [Text Services Framework],EnumCandidates method, ITfCandidateList.EnumCandidates, ITfCandidateList::EnumCandidates, _tsf_itfcandidatelist_enumcandidates_ref, ctffunc/ITfCandidateList::EnumCandidates, tsf.itfcandidatelist_enumcandidates
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
 - ITfCandidateList.EnumCandidates
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCandidateList::EnumCandidates


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms538125(v=VS.85).aspx">IEnumTfCandidates</a> interface pointer that receives the enumerator object. The caller must release this interface when it is no longer required.


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
<i>ppEnum</i> is invalid.

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




<a href="https://msdn.microsoft.com/4daef7e9-e5ab-4eb8-acb6-a475b84d4de6">IEnumTfCandidates
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms538492(v=VS.85).aspx">ITfCandidateList</a>
 

 

