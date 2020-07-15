---
UID: NN:bdaiface.IBDA_UserActivityService
title: IBDA_UserActivityService (bdaiface.h)
description: Defines methods that detect user activity in a Protected Broadcast Driver Architecture (PBDA) media graph.
helpviewer_keywords: ["IBDA_UserActivityService","IBDA_UserActivityService interface [Microsoft TV Technologies]","IBDA_UserActivityService interface [Microsoft TV Technologies]","described","bdaiface/IBDA_UserActivityService","mstv.ibda_useractivityservice"]
old-location: mstv\ibda_useractivityservice.htm
tech.root: mstv
ms.assetid: d2c8f14e-11d7-4385-a6c8-31b086ec1286
ms.date: 12/05/2018
ms.keywords: IBDA_UserActivityService, IBDA_UserActivityService interface [Microsoft TV Technologies], IBDA_UserActivityService interface [Microsoft TV Technologies],described, bdaiface/IBDA_UserActivityService, mstv.ibda_useractivityservice
f1_keywords:
- bdaiface/IBDA_UserActivityService
dev_langs:
- c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdaiface.h
api_name:
- IBDA_UserActivityService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_UserActivityService interface


## -description


Defines methods that detect user activity in a Protected Broadcast Driver Architecture (PBDA) media graph.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_UserActivityService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_UserActivityService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_UserActivityService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_useractivityservice-getuseractivityinterval">GetUserActivityInterval</a>
</td>
<td align="left" width="63%">
Gets or sets the timeout interval for a Media Sink Device (MSD) to inform a Media Transfer Device (MTD) about user activity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_useractivityservice-setcurrenttunerusereason">SetCurrentTunerUseReason</a>
</td>
<td align="left" width="63%">
Specifies the reason for user activity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_useractivityservice-useractivitydetected">UserActivityDetected</a>
</td>
<td align="left" width="63%">
Tells an MTD that user activity has occured.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_UserActivityService)</code>.



