---
UID: NN:bdaiface.IBDA_FrequencyFilter
title: IBDA_FrequencyFilter
author: windows-sdk-content
description: The IBDA_FrequencyFilter interface is implemented on a BDA tuner device, and is used by the Network Provider to tell the tuner how to set its frequencies.
old-location: mstv\ibda_frequencyfilter.htm
old-project: mstv
ms.assetid: ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBDA_FrequencyFilter, IBDA_FrequencyFilter interface [Microsoft TV Technologies], IBDA_FrequencyFilter interface [Microsoft TV Technologies],described, IBDA_FrequencyFilterInterface, bdaiface/IBDA_FrequencyFilter, mstv.ibda_frequencyfilter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_FrequencyFilter</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBDA_FrequencyFilter</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693356(v=VS.85).aspx">get_Autotune</a>
</td>
<td align="left" width="63%">
Retrieves a channel frequency to scan for a precise signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693357(v=VS.85).aspx">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693358(v=VS.85).aspx">get_Frequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693359(v=VS.85).aspx">get_FrequencyMultiplier</a>
</td>
<td align="left" width="63%">
Retrieves the frequency multiplier parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693360(v=VS.85).aspx">get_Polarity</a>
</td>
<td align="left" width="63%">
Retrieves the polarity parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693361(v=VS.85).aspx">get_Range</a>
</td>
<td align="left" width="63%">
Retrieves the tuner range parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693362(v=VS.85).aspx">put_Autotune</a>
</td>
<td align="left" width="63%">
Specifies a channel frequency to scans for a precise signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693363(v=VS.85).aspx">put_Bandwidth</a>
</td>
<td align="left" width="63%">
Specifies the bandwidth parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693364(v=VS.85).aspx">put_Frequency</a>
</td>
<td align="left" width="63%">
Specifies the frequency parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693365(v=VS.85).aspx">put_FrequencyMultiplier</a>
</td>
<td align="left" width="63%">
Specifies the frequency multiplier parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693366(v=VS.85).aspx">put_Polarity</a>
</td>
<td align="left" width="63%">
Specifies the polarity parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693367(v=VS.85).aspx">put_Range</a>
</td>
<td align="left" width="63%">
Specifies the tuner range parameters

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_FrequencyFilter)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693008(v=VS.85).aspx">BDA Interfaces</a>
 

 

