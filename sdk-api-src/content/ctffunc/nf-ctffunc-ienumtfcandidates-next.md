---
UID: NF:ctffunc.IEnumTfCandidates.Next
title: IEnumTfCandidates::Next
author: windows-sdk-content
description: IEnumTfCandidates::Next method
old-location: tsf\ienumtfcandidates_next.htm
old-project: TSF
ms.assetid: 50aaa3c0-6998-49de-9753-7be38625a10d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEnumTfCandidates interface [Text Services Framework],Next method, IEnumTfCandidates.Next, IEnumTfCandidates::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfCandidates interface, _tsf_ienumtfcandidates_next_ref, ctffunc/IEnumTfCandidates::Next, tsf.ienumtfcandidates_next
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IEnumTfCandidates.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# IEnumTfCandidates::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param ppCand [out]

Pointer to an array of <a href="https://msdn.microsoft.com/82c77b59-a50c-42ae-ba1d-25a1c196662d">ITfCandidateString</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


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




<a href="https://msdn.microsoft.com/4daef7e9-e5ab-4eb8-acb6-a475b84d4de6">IEnumTfCandidates</a>



<a href="https://msdn.microsoft.com/82c77b59-a50c-42ae-ba1d-25a1c196662d">ITfCandidateString
      </a>
 

 

