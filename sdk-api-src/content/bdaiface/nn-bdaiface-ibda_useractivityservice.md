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
<a href="https://msdn.microsoft.com/2ea3504a-a479-4d26-8a6b-0e5bdddf6a21">GetUserActivityInterval</a>
</td>
<td align="left" width="63%">
Gets or sets the timeout interval for a Media Sink Device (MSD) to inform a Media Transfer Device (MTD) about user activity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/248a0b01-02be-49b3-88ff-3b830d77e08d">SetCurrentTunerUseReason</a>
</td>
<td align="left" width="63%">
Specifies the reason for user activity.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24c5f6af-602d-4e96-9712-5444ffdd4fe6">UserActivityDetected</a>
</td>
<td align="left" width="63%">
Tells an MTD that user activity has occured.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_UserActivityService)</code>.



