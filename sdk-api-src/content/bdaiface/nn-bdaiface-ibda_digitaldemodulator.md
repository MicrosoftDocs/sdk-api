---
UID: NN:bdaiface.IBDA_DigitalDemodulator
title: IBDA_DigitalDemodulator (bdaiface.h)
description: The IBDA_DigitalDemodulator interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal.helpviewer_keywords: ["IBDA_DigitalDemodulator","IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","IBDA_DigitalDemodulator interface [Microsoft TV Technologies]","described","IBDA_DigitalDemodulatorInterface","bdaiface/IBDA_DigitalDemodulator","mstv.ibda_digitaldemodulator"]
old-location: mstv\ibda_digitaldemodulator.htm
tech.root: mstv
ms.assetid: 13ecd348-dc2b-4e80-9875-927f4ed55c95
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator, IBDA_DigitalDemodulator interface [Microsoft TV Technologies], IBDA_DigitalDemodulator interface [Microsoft TV Technologies],described, IBDA_DigitalDemodulatorInterface, bdaiface/IBDA_DigitalDemodulator, mstv.ibda_digitaldemodulator
f1_keywords:
- bdaiface/IBDA_DigitalDemodulator
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
- IBDA_DigitalDemodulator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_DigitalDemodulator interface


## -description



The <b>IBDA_DigitalDemodulator</b> interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal. A Network Provider calls these methods on the filter to provide the demodulator with the information it needs to acquire a particular signal. The Network Provider obtains these values from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695081(v=vs.85)">Locator</a> object associated with the tune request or tuning space.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DigitalDemodulator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_DigitalDemodulator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_DigitalDemodulator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_innerfecmethod">get_InnerFECMethod</a>
</td>
<td align="left" width="63%">
Retrieves the inner forward error correction method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_innerfecrate">get_InnerFECRate</a>
</td>
<td align="left" width="63%">
Retrieves the inner forward error correction rate being used on the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/modulationtype">get_ModulationType</a>
</td>
<td align="left" width="63%">
Retrieves the modulation type for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_outerfecmethod">get_OuterFECMethod</a>
</td>
<td align="left" width="63%">
Retrieves the outer forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_outerfecrate">get_OuterFECRate</a>
</td>
<td align="left" width="63%">
Retrieves the outer forward error correction rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/spectralinversion">get_SpectralInversion</a>
</td>
<td align="left" width="63%">
Retrieves the spectral inversion value for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-get_symbolrate">get_SymbolRate</a>
</td>
<td align="left" width="63%">
Retrieves the symbol rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_innerfecmethod">put_InnerFECMethod</a>
</td>
<td align="left" width="63%">
Specifies the inner forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_innerfecrate">put_InnerFECRate</a>
</td>
<td align="left" width="63%">
Specifies the inner forward error correction rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_modulationtype">put_ModulationType</a>
</td>
<td align="left" width="63%">
Specifies the modulation type for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_outerfecmethod">put_OuterFECMethod</a>
</td>
<td align="left" width="63%">
Specifies the outer forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_outerfecrate">put_OuterFECRate</a>
</td>
<td align="left" width="63%">
Specifies the outer forward error correction rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_spectralinversion">put_SpectralInversion</a>
</td>
<td align="left" width="63%">
Specifies the spectral inversion value for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_digitaldemodulator-put_symbolrate">put_SymbolRate</a>
</td>
<td align="left" width="63%">
Specifies the symbol rate for the signal.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DigitalDemodulator)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

