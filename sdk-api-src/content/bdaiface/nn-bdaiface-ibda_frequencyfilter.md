---
UID: NN:bdaiface.IBDA_FrequencyFilter
title: IBDA_FrequencyFilter
author: windows-sdk-content
description: The IBDA_FrequencyFilter interface is implemented on a BDA tuner device, and is used by the Network Provider to tell the tuner how to set its frequencies.
old-location: mstv\ibda_frequencyfilter.htm
old-project: mstv
ms.assetid: ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_FrequencyFilter, IBDA_FrequencyFilter interface [Microsoft TV Technologies], IBDA_FrequencyFilter interface [Microsoft TV Technologies],described, IBDA_FrequencyFilterInterface, bdaiface/IBDA_FrequencyFilter, mstv.ibda_frequencyfilter
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_FrequencyFilter
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_FrequencyFilter interface


## -description



The <b>IBDA_FrequencyFilter</b> interface is implemented on a BDA tuner device, and is used by the Network Provider to tell the tuner how to set its frequencies.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_FrequencyFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_FrequencyFilter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_FrequencyFilter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/146c4499-a8e9-4794-ab6c-b8e0e73ebad1">get_Autotune</a>
</td>
<td align="left" width="63%">
Retrieves a channel frequency to scan for a precise signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cea7bbe-488b-4c5c-84a8-28f0dc77e3c1">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eba0f92-45a7-4c5e-9450-f3c7a176288c">get_Frequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/463a58f7-a10c-40b5-8183-3e16bcc7c6b2">get_FrequencyMultiplier</a>
</td>
<td align="left" width="63%">
Retrieves the frequency multiplier parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1f787f6-5d52-44a0-90d7-c905b7e8b8b1">get_Polarity</a>
</td>
<td align="left" width="63%">
Retrieves the polarity parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fdf96400-8fd9-4989-9977-026a9bec37ea">get_Range</a>
</td>
<td align="left" width="63%">
Retrieves the tuner range parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2ca03b8-fd22-4b8f-90a9-42a235b0a675">put_Autotune</a>
</td>
<td align="left" width="63%">
Specifies a channel frequency to scans for a precise signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e44a5b4-c3ea-4afa-aab3-4f6732a3bd82">put_Bandwidth</a>
</td>
<td align="left" width="63%">
Specifies the bandwidth parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70d50a4b-b0f8-42a1-9fa2-1d09376903fe">put_Frequency</a>
</td>
<td align="left" width="63%">
Specifies the frequency parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b67bd442-26cf-4104-906c-e9510b99ad90">put_FrequencyMultiplier</a>
</td>
<td align="left" width="63%">
Specifies the frequency multiplier parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d15bd0f9-4f2e-4098-bf5b-db03fde1362f">put_Polarity</a>
</td>
<td align="left" width="63%">
Specifies the polarity parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3567c723-13ef-4306-81dd-2e844abeeb04">put_Range</a>
</td>
<td align="left" width="63%">
Specifies the tuner range parameters

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_FrequencyFilter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

