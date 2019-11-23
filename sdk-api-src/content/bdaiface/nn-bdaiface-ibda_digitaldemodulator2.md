---
UID: NN:bdaiface.IBDA_DigitalDemodulator2
title: IBDA_DigitalDemodulator2 (bdaiface.h)

description: Controls a Broadcast Driver Architecture (BDA) demodulator filter. Demodulation filters for Digital Video Broadcasting-Satellite version 2 (DVB-S2) implement this interface.
old-location: mstv\ibda_digitaldemodulator2.htm
tech.root: mstv
ms.assetid: 337fba05-80d5-4638-9936-2e02767a5b1b

ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator2, IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies], IBDA_DigitalDemodulator2 interface [Microsoft TV Technologies],described, bdaiface/IBDA_DigitalDemodulator2, mstv.ibda_digitaldemodulator2
ms.topic: interface
f1_keywords: 
 - "bdaiface/IBDA_DigitalDemodulator2"
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
req.idl: Bdaiface.idl
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
 - IBDA_DigitalDemodulator2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_DigitalDemodulator2 interface


## -description


Controls a Broadcast Driver Architecture (BDA) demodulator filter. Demodulation filters for Digital Video Broadcasting-Satellite version 2 (DVB-S2) implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DigitalDemodulator2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nn-bdaiface-ibda_digitaldemodulator">IBDA_DigitalDemodulator</a>. <b>IBDA_DigitalDemodulator2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_DigitalDemodulator2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator2-get_guardinterval">get_GuardInterval</a>
</td>
<td align="left" width="63%">
Gets the demodulator's guard interval.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/pilot">get_Pilot</a>
</td>
<td align="left" width="63%">
Gets the current pilot mode for Digital Video Broadcasting-S2 (DVB-S2).
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/rolloff">get_RollOff</a>
</td>
<td align="left" width="63%">
Gets the demodulator's roll-off factor.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/transmissionmode">get_TransmissionMode</a>
</td>
<td align="left" width="63%">
Gets the demodulator's transmission mode.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator2-put_guardinterval">put_GuardInterval</a>
</td>
<td align="left" width="63%">
Sets the demodulator's guard interval.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator2-put_pilot">put_Pilot</a>
</td>
<td align="left" width="63%">
Sets the current pilot mode for DVB-S2.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator2-put_rolloff">put_RollOff</a>
</td>
<td align="left" width="63%">
Sets the demodulator's roll-off factor.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator2-put_transmissionmode">put_TransmissionMode</a>
</td>
<td align="left" width="63%">
Sets the demodulator's transmission mode.
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DigitalDemodulator2)</code>.



