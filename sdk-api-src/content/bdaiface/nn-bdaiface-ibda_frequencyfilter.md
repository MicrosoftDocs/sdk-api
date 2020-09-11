---
UID: NN:bdaiface.IBDA_FrequencyFilter
title: IBDA_FrequencyFilter (bdaiface.h)
description: The IBDA_FrequencyFilter interface is implemented on a BDA tuner device, and is used by the Network Provider to tell the tuner how to set its frequencies.
helpviewer_keywords: ["IBDA_FrequencyFilter","IBDA_FrequencyFilter interface [Microsoft TV Technologies]","IBDA_FrequencyFilter interface [Microsoft TV Technologies]","described","IBDA_FrequencyFilterInterface","bdaiface/IBDA_FrequencyFilter","mstv.ibda_frequencyfilter"]
old-location: mstv\ibda_frequencyfilter.htm
tech.root: mstv
ms.assetid: ef5dbf4a-ecbb-4f2c-a34d-ce3864133adc
ms.date: 12/05/2018
ms.keywords: IBDA_FrequencyFilter, IBDA_FrequencyFilter interface [Microsoft TV Technologies], IBDA_FrequencyFilter interface [Microsoft TV Technologies],described, IBDA_FrequencyFilterInterface, bdaiface/IBDA_FrequencyFilter, mstv.ibda_frequencyfilter
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_FrequencyFilter
 - bdaiface/IBDA_FrequencyFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_FrequencyFilter
---

# IBDA_FrequencyFilter interface


## -description

The <b>IBDA_FrequencyFilter</b> interface is implemented on a BDA tuner device, and is used by the Network Provider to tell the tuner how to set its frequencies.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_FrequencyFilter</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_FrequencyFilter</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_autotune">get_Autotune</a>
</td>
<td align="left" width="63%">
Retrieves a channel frequency to scan for a precise signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_bandwidth">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequency">get_Frequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_frequencymultiplier">get_FrequencyMultiplier</a>
</td>
<td align="left" width="63%">
Retrieves the frequency multiplier parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_polarity">get_Polarity</a>
</td>
<td align="left" width="63%">
Retrieves the polarity parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-get_range">get_Range</a>
</td>
<td align="left" width="63%">
Retrieves the tuner range parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_autotune">put_Autotune</a>
</td>
<td align="left" width="63%">
Specifies a channel frequency to scans for a precise signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_bandwidth">put_Bandwidth</a>
</td>
<td align="left" width="63%">
Specifies the bandwidth parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_frequency">put_Frequency</a>
</td>
<td align="left" width="63%">
Specifies the frequency parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_frequencymultiplier">put_FrequencyMultiplier</a>
</td>
<td align="left" width="63%">
Specifies the frequency multiplier parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_polarity">put_Polarity</a>
</td>
<td align="left" width="63%">
Specifies the polarity parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_frequencyfilter-put_range">put_Range</a>
</td>
<td align="left" width="63%">
Specifies the tuner range parameters

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_FrequencyFilter)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>

