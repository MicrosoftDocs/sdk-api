---
UID: NF:winsatcominterfacei.IInitiateWinSATAssessment.CancelAssessment
title: IInitiateWinSATAssessment::CancelAssessment
author: windows-driver-content
description: Cancels a currently running assessment.
old-location: winsat\iinitiatewinsatassessment_cancelassessment.htm
old-project: WinSAT
ms.assetid: fa4b159f-9d40-445f-bd43-5fc2e7b2d33b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CancelAssessment, CancelAssessment method [WinSAT], CancelAssessment method [WinSAT],IInitiateWinSATAssessment interface, IInitiateWinSATAssessment interface [WinSAT],CancelAssessment method, IInitiateWinSATAssessment.CancelAssessment, IInitiateWinSATAssessment::CancelAssessment, winsat.iinitiatewinsatassessment_cancelassessment, winsatcominterfacei/IInitiateWinSATAssessment::CancelAssessment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsatcominterfacei.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Winsatapi.dll
api_name:
-	IInitiateWinSATAssessment.CancelAssessment
product: Windows
targetos: Windows
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IInitiateWinSATAssessment::CancelAssessment


## -description


<p class="CCE_Message">[IInitiateWinSATAssessment::CancelAssessment may be altered or unavailable for releases after Windows 8.1.]

Cancels a currently running assessment.


## -parameters






## -returns



Returns S_OK if successful; otherwise, the method returns the following error code or a Win32 error code returned as an HRESULT.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINSAT_ERROR_WINSAT_NOT_RUNNING</b></dt>
<dt>0x80040006</dt>
</dl>
</td>
<td width="60%">
There is no running assessment to cancel.

</td>
</tr>
</table>
 




## -remarks



This method sends WinSAT a request to cancel the assessment. To determine if the cancel request succeeded, implement the <a href="https://msdn.microsoft.com/a7bcd7e6-b8d7-4ec3-84e8-8ccbcd0b4ada">IWinSATInitiateEvents::WinSATComplete</a> method and check the <i>hresult</i> parameter for a value of WINSAT_ERROR_WINSAT_CANCELED.




## -see-also




<a href="https://msdn.microsoft.com/0b299477-50a4-4f61-a0e5-fdbae239503b">IInitiateWinSATAssessment</a>



<a href="https://msdn.microsoft.com/c57d88b6-81ac-4314-8593-59a950348be4">IInitiateWinSATAssessment::InitiateAssessment</a>



<a href="https://msdn.microsoft.com/9425e41c-fe03-4c94-a5eb-686775b5fce7">IInitiateWinSATAssessment::InitiateFormalAssessment</a>
 

 

