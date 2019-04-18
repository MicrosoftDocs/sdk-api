---
UID: NN:segment.IMSVidAnalogTuner
title: IMSVidAnalogTuner (segment.h)
author: windows-sdk-content
description: The IMSVidAnalogTuner interface represents an analog-only tuner card that does not support the Broadcast Driver Architecture (BDA). This interface provides Automation access to the IAMTVTuner and IAMTVAudio interfaces.
old-location: mstv\imsvidanalogtuner.htm
tech.root: mstv
ms.assetid: 640143d3-6712-4e92-a1d9-0689637b3d90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidAnalogTuner, IMSVidAnalogTuner interface [Microsoft TV Technologies], IMSVidAnalogTuner interface [Microsoft TV Technologies],described, IMSVidAnalogTunerInterface, mstv.imsvidanalogtuner, segment/IMSVidAnalogTuner
ms.topic: interface
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - segment.h
api_name:
 - IMSVidAnalogTuner
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidAnalogTuner interface


## -description



The <b>IMSVidAnalogTuner</b> interface represents an analog-only tuner card that does not support the Broadcast Driver Architecture (BDA). This interface provides Automation access to the <a href="https://msdn.microsoft.com/en-us/library/Dd375971(v=VS.85).aspx">IAMTVTuner</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd375962(v=VS.85).aspx">IAMTVAudio</a> interfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidAnalogTuner</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd694704(v=VS.85).aspx">IMSVidTuner</a>. <b>IMSVidAnalogTuner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidAnalogTuner</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694426(v=VS.85).aspx">ChannelAvailable</a>
</td>
<td align="left" width="63%">
Queries whether a specified channel is available for viewing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694427(v=VS.85).aspx">get_AudioFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's audio frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694428(v=VS.85).aspx">get_Channel</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's channel setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694429(v=VS.85).aspx">get_CountryCode</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694430(v=VS.85).aspx">get_SAP</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's SAP setting to enable secondary audio components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694431(v=VS.85).aspx">get_VideoFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's video frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694432(v=VS.85).aspx">put_Channel</a>
</td>
<td align="left" width="63%">
Specifies the tuner's channel setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694433(v=VS.85).aspx">put_CountryCode</a>
</td>
<td align="left" width="63%">
Specifies the tuner's country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd694434(v=VS.85).aspx">put_SAP</a>
</td>
<td align="left" width="63%">
Specifies the tuner's SAP setting to enable secondary audio components.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAnalogTuner)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd694704(v=VS.85).aspx">IMSVidTuner</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

