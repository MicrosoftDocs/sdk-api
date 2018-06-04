---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

