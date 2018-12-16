---
UID: NN:bdaiface.IBDA_LNBInfo
title: IBDA_LNBInfo
author: windows-sdk-content
description: The IBDA_LNBInfo interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.
old-location: mstv\ibda_lnbinfo.htm
tech.root: mstv
ms.assetid: 4985b525-c000-4d19-9679-c995cbc3c99b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_LNBInfo, IBDA_LNBInfo interface [Microsoft TV Technologies], IBDA_LNBInfo interface [Microsoft TV Technologies],described, IBDA_LNBInfoInterface, bdaiface/IBDA_LNBInfo, mstv.ibda_lnbinfo
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693397(v=VS.85).aspx">get_HighLowSwitchFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency of the high-low switch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693398(v=VS.85).aspx">get_LocalOscilatorFrequencyHighBand</a>
</td>
<td align="left" width="63%">
Retrieves the high band of the local oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693399(v=VS.85).aspx">get_LocalOscilatorFrequencyLowBand</a>
</td>
<td align="left" width="63%">
Retrieves the low band of the local oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693400(v=VS.85).aspx">put_HighLowSwitchFrequency</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the high-low switch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693401(v=VS.85).aspx">put_LocalOscilatorFrequencyHighBand</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the local oscillator high band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693402(v=VS.85).aspx">put_LocalOscilatorFrequencyLowBand</a>
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
 

 

