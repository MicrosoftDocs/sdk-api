---
UID: NN:bdaiface.IBDA_LNBInfo
title: IBDA_LNBInfo
author: windows-sdk-content
description: The IBDA_LNBInfo interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.
old-location: mstv\ibda_lnbinfo.htm
tech.root: MSTV
ms.assetid: 4985b525-c000-4d19-9679-c995cbc3c99b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IBDA_LNBInfo, IBDA_LNBInfo interface [Microsoft TV Technologies], IBDA_LNBInfo interface [Microsoft TV Technologies],described, IBDA_LNBInfoInterface, bdaiface/IBDA_LNBInfo, mstv.ibda_lnbinfo
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
 - IBDA_LNBInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_LNBInfo interface


## -description



The <b>IBDA_LNBInfo</b> interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_LNBInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_LNBInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_LNBInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6a851fc-6911-41fb-951c-c9fcf04b2355">get_HighLowSwitchFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency of the high-low switch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21960718-818c-4efb-a2c2-577c3b938da4">get_LocalOscilatorFrequencyHighBand</a>
</td>
<td align="left" width="63%">
Retrieves the high band of the local oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aabb13a-166f-4b50-90a5-a18dd4b04720">get_LocalOscilatorFrequencyLowBand</a>
</td>
<td align="left" width="63%">
Retrieves the low band of the local oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3edde05f-1cdb-4648-a34b-ba95e4fcff12">put_HighLowSwitchFrequency</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the high-low switch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a1de764-aaab-4801-ba34-65c05d245ba0">put_LocalOscilatorFrequencyHighBand</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the local oscillator high band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1ba4cf7-f9d4-4cac-921f-19f34fd968fe">put_LocalOscilatorFrequencyLowBand</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the local oscillator's low band.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_LNBInfo)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

