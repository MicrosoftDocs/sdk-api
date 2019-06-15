---
UID: NN:winsatcominterfacei.IWinSATInitiateEvents
title: IWinSATInitiateEvents (winsatcominterfacei.h)
author: windows-sdk-content
description: Implement this interface to receive notifications when an assessment is complete or making progress.
old-location: winsat\iwinsatinitiateevents.htm
tech.root: WinSAT
ms.assetid: f6ab3284-a76f-4148-ae40-04aa782ea9a7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWinSATInitiateEvents, IWinSATInitiateEvents interface [WinSAT], IWinSATInitiateEvents interface [WinSAT],described, winsat.iwinsatinitiateevents, winsatcominterfacei/IWinSATInitiateEvents
ms.topic: interface
f1_keywords: ["winsatcominterfacei/IWinSATInitiateEvents"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsatapi.dll
api_name:
 - IWinSATInitiateEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWinSATInitiateEvents interface


## -description


<p class="CCE_Message">[IWinSATInitiateEvents may be altered or unavailable for releases after Windows 8.1.]

Implement this interface to receive notifications when an assessment is complete or making progress.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWinSATInitiateEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWinSATInitiateEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWinSATInitiateEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iwinsatinitiateevents-winsatcomplete">WinSATComplete</a>
</td>
<td align="left" width="63%">
Receives notification  when an assessment succeeds, fails, or is canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iwinsatinitiateevents-winsatupdate">WinSATUpdate</a>
</td>
<td align="left" width="63%">
Receives notification  when an assessment is making progress.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateassessment">IInitiateWinSATAssessment::InitiateAssessment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsatcominterfacei/nf-winsatcominterfacei-iinitiatewinsatassessment-initiateformalassessment">IInitiateWinSATAssessment::InitiateFormalAssessment</a>
 

 

