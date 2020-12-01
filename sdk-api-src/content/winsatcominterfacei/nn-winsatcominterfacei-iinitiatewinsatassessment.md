---
UID: NN:winsatcominterfacei.IInitiateWinSATAssessment
title: IInitiateWinSATAssessment (winsatcominterfacei.h)
description: Initiates an assessment.
helpviewer_keywords: ["IInitiateWinSATAssessment","IInitiateWinSATAssessment interface [WinSAT]","IInitiateWinSATAssessment interface [WinSAT]","described","winsat.iinitiatewinsatassessment","winsatcominterfacei/IInitiateWinSATAssessment"]
old-location: winsat\iinitiatewinsatassessment.htm
tech.root: WinSAT
ms.assetid: 0b299477-50a4-4f61-a0e5-fdbae239503b
ms.date: 12/05/2018
ms.keywords: IInitiateWinSATAssessment, IInitiateWinSATAssessment interface [WinSAT], IInitiateWinSATAssessment interface [WinSAT],described, winsat.iinitiatewinsatassessment, winsatcominterfacei/IInitiateWinSATAssessment
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
 - IInitiateWinSATAssessment
 - winsatcominterfacei/IInitiateWinSATAssessment
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
 - IInitiateWinSATAssessment
---

# IInitiateWinSATAssessment interface


## -description

<p class="CCE_Message">[IInitiateWinSATAssessment may be altered or unavailable for releases after Windows 8.1.]

Initiates an assessment.

To retrieve this interface, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function. Use __uuidof(CInitiateWinSAT) as the class identifier and __uuidof(IInitiateWinSATAssessment) as the interface identifier.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitiateWinSATAssessment</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitiateWinSATAssessment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitiateWinSATAssessment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-cancelassessment">CancelAssessment</a>
</td>
<td align="left" width="63%">
Cancels a currently running assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment">InitiateAssessment</a>
</td>
<td align="left" width="63%">
Initiates an ad hoc assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment">InitiateFormalAssessment</a>
</td>
<td align="left" width="63%">
Initiates a formal assessment.

</td>
</tr>
</table>