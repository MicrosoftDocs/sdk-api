---
UID: NN:segment.IMSVidAnalogTuner
title: IMSVidAnalogTuner
author: windows-driver-content
description: The IMSVidAnalogTuner interface represents an analog-only tuner card that does not support the Broadcast Driver Architecture (BDA). This interface provides Automation access to the IAMTVTuner and IAMTVAudio interfaces.
old-location: mstv\imsvidanalogtuner.htm
old-project: mstv
ms.assetid: 640143d3-6712-4e92-a1d9-0689637b3d90
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMSVidAnalogTuner, IMSVidAnalogTuner interface [Microsoft TV Technologies], IMSVidAnalogTuner interface [Microsoft TV Technologies], described, IMSVidAnalogTunerInterface, mstv.imsvidanalogtuner, segment/IMSVidAnalogTuner
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidAnalogTuner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IMSVidAnalogTuner interface


## -description



The <b>IMSVidAnalogTuner</b> interface represents an analog-only tuner card that does not support the Broadcast Driver Architecture (BDA). This interface provides Automation access to the <a href="https://msdn.microsoft.com/1c8300c2-be13-4e4c-aa0c-53ce57bc9152">IAMTVTuner</a> and <a href="https://msdn.microsoft.com/de340594-4410-4896-b206-0f47d4035bc1">IAMTVAudio</a> interfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidAnalogTuner</b> interface inherits from <a href="https://msdn.microsoft.com/b11f3ac4-c351-4017-9801-98d8edec7449">IMSVidTuner</a>. <b>IMSVidAnalogTuner</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/67533d80-6026-434f-a20f-ded3c119d318">ChannelAvailable</a>
</td>
<td align="left" width="63%">
Queries whether a specified channel is available for viewing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0513ea0-305b-40ac-95ad-ed47a0417046">get_AudioFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's audio frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d62cd70-02cf-4454-b5b7-da2d623ec95d">get_Channel</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's channel setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8efd47f-2a89-4982-88dd-3bfc6c00801b">get_CountryCode</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9943ca7e-754e-4145-8f52-0a915fd7133d">get_SAP</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's SAP setting to enable secondary audio components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6ed5c47-c2cb-4025-9b93-57db25b5cec5">get_VideoFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the tuner's video frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1afd718d-bca9-478c-b56e-413de0f15656">put_Channel</a>
</td>
<td align="left" width="63%">
Specifies the tuner's channel setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6ec6975-8953-45df-9d86-cf8b8888bba6">put_CountryCode</a>
</td>
<td align="left" width="63%">
Specifies the tuner's country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e27efb36-de0c-4255-a5d8-6357f283cd12">put_SAP</a>
</td>
<td align="left" width="63%">
Specifies the tuner's SAP setting to enable secondary audio components.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidAnalogTuner)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b11f3ac4-c351-4017-9801-98d8edec7449">IMSVidTuner</a>



<a href="https://msdn.microsoft.com/bf6c3ce9-1e56-4109-93f1-5b313e6ca19b">Video Control Interfaces</a>
 

 

