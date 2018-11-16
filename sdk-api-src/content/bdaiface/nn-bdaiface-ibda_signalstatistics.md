---
UID: NN:bdaiface.IBDA_SignalStatistics
title: IBDA_SignalStatistics
author: windows-sdk-content
description: The IBDA_SignalStatistics interface is implemented on a BDA device filter and provides methods by which the filter can describe the condition of a signal that is being received.
old-location: mstv\ibda_signalstatistics.htm
tech.root: mstv
ms.assetid: ee8b25d5-d39b-42ac-9f6a-0825e396241c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IBDA_SignalStatistics, IBDA_SignalStatistics interface [Microsoft TV Technologies], IBDA_SignalStatistics interface [Microsoft TV Technologies],described, IBDA_SignalStatisticsInterface, bdaiface/IBDA_SignalStatistics, mstv.ibda_signalstatistics
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
 - IBDA_SignalStatistics
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_SignalStatistics interface


## -description



The <b>IBDA_SignalStatistics</b> interface is implemented on a BDA device filter and provides methods by which the filter can describe the condition of a signal that is being received.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_SignalStatistics</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_SignalStatistics</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_SignalStatistics</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9651e393-224b-4276-b8a6-f841f9e04d48">get_SampleTime</a>
</td>
<td align="left" width="63%">
Retrieves the sample time used to measure the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a67ff4b-1abc-43c4-b171-f9af90c5aaf7">get_SignalLocked</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value indicating whether the signal is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834149e1-50b7-42f6-8fee-a357ed4bc8b8">get_SignalPresent</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value indicating whether a signal is present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2472a539-e8ee-4501-b7ab-e7e1fce7cea0">get_SignalQuality</a>
</td>
<td align="left" width="63%">
Retrieves a value from 1 to 100 indicating the quality of the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4830da1-1031-456e-8f3f-eb15f5366942">get_SignalStrength</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the strength of the signal in decibels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/086fd3ad-26d7-4b5b-b73a-a7d4db44d2c2">put_SampleTime</a>
</td>
<td align="left" width="63%">
Specifies the sample time used to measure the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26e4053f-7e43-464d-8ea1-076f741d5b63">put_SignalLocked</a>
</td>
<td align="left" width="63%">
Specifies whether the signal is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d27dd06-a180-4ee6-bb52-34a8f434ab6a">put_SignalPresent</a>
</td>
<td align="left" width="63%">
Specifies whether a signal is present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7d73965-4f7e-4330-89f4-2ccbe679ae2a">put_SignalQuality</a>
</td>
<td align="left" width="63%">
Specifies the quality of the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3a1f11b7-09f4-430a-8976-81f15ea22b1a">put_SignalStrength</a>
</td>
<td align="left" width="63%">
Specifies the strength of the signal in decibels.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_SignalStatistics)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

