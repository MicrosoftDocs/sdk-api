---
UID: NN:bdaiface.IBDA_UserActivityService
title: IBDA_UserActivityService
author: windows-sdk-content
description: Defines methods that detect user activity in a Protected Broadcast Driver Architecture (PBDA) media graph.
old-location: mstv\ibda_useractivityservice.htm
tech.root: mstv
ms.assetid: d2c8f14e-11d7-4385-a6c8-31b086ec1286
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_UserActivityService, IBDA_UserActivityService interface [Microsoft TV Technologies], IBDA_UserActivityService interface [Microsoft TV Technologies],described, bdaiface/IBDA_UserActivityService, mstv.ibda_useractivityservice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_UserActivityService interface


## -description


Defines methods that detect user activity in a Protected Broadcast Driver Architecture (PBDA) media graph.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_UserActivityService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_UserActivityService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd797935(v=VS.85).aspx">GetUserActivityInterval</a>
</td>
<td align="left" width="63%">
Gets or sets the timeout interval for a Media Sink Device (MSD) to inform a Media Transfer Device (MTD) about user activity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd797938(v=VS.85).aspx">SetCurrentTunerUseReason</a>
</td>
<td align="left" width="63%">
Specifies the reason for user activity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd797940(v=VS.85).aspx">UserActivityDetected</a>
</td>
<td align="left" width="63%">
Tells an MTD that user activity has occured.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_UserActivityService)</code>.



