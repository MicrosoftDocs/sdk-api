---
UID: NN:bdaiface.IBDA_LNBInfo
title: IBDA_LNBInfo (bdaiface.h)
description: The IBDA_LNBInfo interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.
helpviewer_keywords: ["IBDA_LNBInfo","IBDA_LNBInfo interface [Microsoft TV Technologies]","IBDA_LNBInfo interface [Microsoft TV Technologies]","described","IBDA_LNBInfoInterface","bdaiface/IBDA_LNBInfo","mstv.ibda_lnbinfo"]
old-location: mstv\ibda_lnbinfo.htm
tech.root: mstv
ms.assetid: 4985b525-c000-4d19-9679-c995cbc3c99b
ms.date: 12/05/2018
ms.keywords: IBDA_LNBInfo, IBDA_LNBInfo interface [Microsoft TV Technologies], IBDA_LNBInfo interface [Microsoft TV Technologies],described, IBDA_LNBInfoInterface, bdaiface/IBDA_LNBInfo, mstv.ibda_lnbinfo
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
 - IBDA_LNBInfo
 - bdaiface/IBDA_LNBInfo
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
 - IBDA_LNBInfo
---

# IBDA_LNBInfo interface


## -description

The <b>IBDA_LNBInfo</b> interface is implemented on a BDA device filter, specifically an LNB device. The methods are called by the Network Provider to instruct the device on how to acquire the satellite signal.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_LNBInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_LNBInfo</b> also has these types of members:
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
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-get_highlowswitchfrequency">get_HighLowSwitchFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the frequency of the high-low switch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-get_localoscilatorfrequencyhighband">get_LocalOscilatorFrequencyHighBand</a>
</td>
<td align="left" width="63%">
Retrieves the high band of the local oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-get_localoscilatorfrequencylowband">get_LocalOscilatorFrequencyLowBand</a>
</td>
<td align="left" width="63%">
Retrieves the low band of the local oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-put_highlowswitchfrequency">put_HighLowSwitchFrequency</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the high-low switch.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-put_localoscilatorfrequencyhighband">put_LocalOscilatorFrequencyHighBand</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the local oscillator high band.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ibda_lnbinfo-put_localoscilatorfrequencylowband">put_LocalOscilatorFrequencyLowBand</a>
</td>
<td align="left" width="63%">
Specifies the frequency of the local oscillator's low band.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_LNBInfo)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>