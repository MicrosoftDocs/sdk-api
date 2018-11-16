---
UID: NN:tuner.IESValueUpdatedEvent
title: IESValueUpdatedEvent
author: windows-sdk-content
description: Implements an event that Protected Broadcast Driver Architecture (PBDA) Media Transform Devices (MTDs) use to inform a Media Sink Device that the MTD has updated the value for a name-value pair or exposed a new name-value pair.
old-location: mstv\iesvalueupdatedevent.htm
tech.root: mstv
ms.assetid: 6639c483-aebe-43b4-94cd-494b820c1b14
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IESValueUpdatedEvent, IESValueUpdatedEvent interface [Microsoft TV Technologies], IESValueUpdatedEvent interface [Microsoft TV Technologies],described, mstv.iesvalueupdatedevent, tuner/IESValueUpdatedEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IESValueUpdatedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESValueUpdatedEvent interface


## -description


Implements an event that Protected Broadcast Driver Architecture (PBDA) Media Transform Devices (MTDs) use to inform a Media Sink Device that the MTD has updated the value for a name-value pair or exposed a new name-value pair. The pair is implemented as part of the PBDA General Purpose Name-Value Service.

For more information about PBDA, download the specification from <a href="http://go.microsoft.com/fwlink/p/?linkid=132926">http://go.microsoft.com/fwlink/p/?linkid=132926</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESValueUpdatedEvent</b> interface inherits from <b>IESEvent</b>. <b>IESValueUpdatedEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESValueUpdatedEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc008b4a-fa6f-4b62-90da-417813081344">GetValueNames</a>
</td>
<td align="left" width="63%">
For a name-value pair in the PBDA General Purpose Name-Value Service, gets the name that has been updated. 


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESValueUpdatedEvent)</code>.



