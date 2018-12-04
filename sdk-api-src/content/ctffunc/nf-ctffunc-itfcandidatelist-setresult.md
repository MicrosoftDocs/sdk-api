---
UID: NF:ctffunc.ITfCandidateList.SetResult
title: ITfCandidateList::SetResult
author: windows-sdk-content
description: ITfCandidateList::SetResult method
old-location: tsf\itfcandidatelist_setresult.htm
tech.root: TSF
ms.assetid: dcc172f9-4fc3-46f4-a1db-0e75fceafb28
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfCandidateList interface [Text Services Framework],SetResult method, ITfCandidateList.SetResult, ITfCandidateList::SetResult, SetResult, SetResult method [Text Services Framework], SetResult method [Text Services Framework],ITfCandidateList interface, _tsf_itfcandidatelist_setresult_ref, ctffunc/ITfCandidateList::SetResult, tsf.itfcandidatelist_setresult
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
 - ITfCandidateList.SetResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCandidateList::SetResult


## -description




## -parameters




### -param nIndex [in]

Specifies the zero-based index of the candidate string to set the result for. This parameter is ignored if <i>imcr</i> contains CAND_CANCELED.


### -param imcr [in]

Contains one of the <a href="https://msdn.microsoft.com/8b2b4762-f28d-40e0-b162-5e35e8835c8e">TfCandidateResult</a> values that specifies the result of the reconversion operation.


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
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



A typical reconversion operation would include the following operations.

<ol>
<li>A list of candidates is obtained and displayed to the user in a dialog box.</li>
<li>When the user selects a candidate, but before the dialog box is dismissed, <b>ITfCandidateList::SetResult</b> is called with the index of the newly selected candidate and CAND_SELECTED.</li>
<li>If a different candidate is selected, <b>ITfCandidateList::SetResult</b> is called agian with the index of the newly selected candidate and CAND_SELECTED.</li>
<li>If the user chooses to accept the new candidate, <b>ITfCandidateList::SetResult</b> is called with the index of the currently selected candidate and CAND_FINALIZED.</li>
<li>If the user cancels the dialog, <b>ITfCandidateList::SetResult</b> is called with an index of zero and CAND_CANCELED.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/e41ba461-6337-4feb-ba16-3942920ebb9f">ITfCandidateList</a>



<a href="https://msdn.microsoft.com/8b2b4762-f28d-40e0-b162-5e35e8835c8e">TfCandidateResult
      </a>
 

 

