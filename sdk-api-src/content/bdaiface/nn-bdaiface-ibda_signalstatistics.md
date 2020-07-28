---
UID: NN:bdaiface.IBDA_SignalStatistics
title: IBDA_SignalStatistics (bdaiface.h)
description: The IBDA_SignalStatistics interface is implemented on a BDA device filter and provides methods by which the filter can describe the condition of a signal that is being received.
helpviewer_keywords: ["IBDA_SignalStatistics","IBDA_SignalStatistics interface [Microsoft TV Technologies]","IBDA_SignalStatistics interface [Microsoft TV Technologies]","described","IBDA_SignalStatisticsInterface","bdaiface/IBDA_SignalStatistics","mstv.ibda_signalstatistics"]
old-location: mstv\ibda_signalstatistics.htm
tech.root: mstv
ms.assetid: ee8b25d5-d39b-42ac-9f6a-0825e396241c
ms.date: 12/05/2018
ms.keywords: IBDA_SignalStatistics, IBDA_SignalStatistics interface [Microsoft TV Technologies], IBDA_SignalStatistics interface [Microsoft TV Technologies],described, IBDA_SignalStatisticsInterface, bdaiface/IBDA_SignalStatistics, mstv.ibda_signalstatistics
f1_keywords:
- bdaiface/IBDA_SignalStatistics
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_SignalStatistics interface


## -description



The <b>IBDA_SignalStatistics</b> interface is implemented on a BDA device filter and provides methods by which the filter can describe the condition of a signal that is being received.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_SignalStatistics</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_SignalStatistics</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_sampletime">get_SampleTime</a>
</td>
<td align="left" width="63%">
Retrieves the sample time used to measure the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signallocked">get_SignalLocked</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value indicating whether the signal is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signalpresent">get_SignalPresent</a>
</td>
<td align="left" width="63%">
Retrieves a Boolean value indicating whether a signal is present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signalquality">get_SignalQuality</a>
</td>
<td align="left" width="63%">
Retrieves a value from 1 to 100 indicating the quality of the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-get_signalstrength">get_SignalStrength</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the strength of the signal in decibels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_sampletime">put_SampleTime</a>
</td>
<td align="left" width="63%">
Specifies the sample time used to measure the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signallocked">put_SignalLocked</a>
</td>
<td align="left" width="63%">
Specifies whether the signal is locked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signalpresent">put_SignalPresent</a>
</td>
<td align="left" width="63%">
Specifies whether a signal is present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signalquality">put_SignalQuality</a>
</td>
<td align="left" width="63%">
Specifies the quality of the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_signalstatistics-put_signalstrength">put_SignalStrength</a>
</td>
<td align="left" width="63%">
Specifies the strength of the signal in decibels.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_SignalStatistics)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

