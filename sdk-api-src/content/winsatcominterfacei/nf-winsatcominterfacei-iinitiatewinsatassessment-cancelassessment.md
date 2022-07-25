---
UID: NF:winsatcominterfacei.IInitiateWinSATAssessment.CancelAssessment
title: IInitiateWinSATAssessment::CancelAssessment (winsatcominterfacei.h)
description: Cancels a currently running assessment.
helpviewer_keywords: ["CancelAssessment","CancelAssessment method [WinSAT]","CancelAssessment method [WinSAT]","IInitiateWinSATAssessment interface","IInitiateWinSATAssessment interface [WinSAT]","CancelAssessment method","IInitiateWinSATAssessment.CancelAssessment","IInitiateWinSATAssessment::CancelAssessment","winsat.iinitiatewinsatassessment_cancelassessment","winsatcominterfacei/IInitiateWinSATAssessment::CancelAssessment"]
old-location: winsat\iinitiatewinsatassessment_cancelassessment.htm
tech.root: WinSAT
ms.assetid: fa4b159f-9d40-445f-bd43-5fc2e7b2d33b
ms.date: 12/05/2018
ms.keywords: CancelAssessment, CancelAssessment method [WinSAT], CancelAssessment method [WinSAT],IInitiateWinSATAssessment interface, IInitiateWinSATAssessment interface [WinSAT],CancelAssessment method, IInitiateWinSATAssessment.CancelAssessment, IInitiateWinSATAssessment::CancelAssessment, winsat.iinitiatewinsatassessment_cancelassessment, winsatcominterfacei/IInitiateWinSATAssessment::CancelAssessment
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
req.lib: 
req.dll: Winsatapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInitiateWinSATAssessment::CancelAssessment
 - winsatcominterfacei/IInitiateWinSATAssessment::CancelAssessment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IInitiateWinSATAssessment.CancelAssessment
---

# IInitiateWinSATAssessment::CancelAssessment


## -description

<p class="CCE_Message">[IInitiateWinSATAssessment::CancelAssessment may be altered or unavailable for releases after Windows 8.1.]

Cancels a currently running assessment.



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

This method sends WinSAT a request to cancel the assessment. To determine if the cancel request succeeded, implement the <a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iwinsatinitiateevents-winsatcomplete">IWinSATInitiateEvents::WinSATComplete</a> method and check the <i>hresult</i> parameter for a value of WINSAT_ERROR_WINSAT_CANCELED.

## -see-also

<a href="/windows/desktop/api/winsatcominterfacei/nn-winsatcominterfacei-iinitiatewinsatassessment">IInitiateWinSATAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment">IInitiateWinSATAssessment::InitiateAssessment</a>



<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment">IInitiateWinSATAssessment::InitiateFormalAssessment</a>
