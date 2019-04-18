---
UID: NN:bdaiface.IBDA_DigitalDemodulator
title: IBDA_DigitalDemodulator (bdaiface.h)
author: windows-sdk-content
description: The IBDA_DigitalDemodulator interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal.
old-location: mstv\ibda_digitaldemodulator.htm
tech.root: mstv
ms.assetid: 13ecd348-dc2b-4e80-9875-927f4ed55c95
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBDA_DigitalDemodulator, IBDA_DigitalDemodulator interface [Microsoft TV Technologies], IBDA_DigitalDemodulator interface [Microsoft TV Technologies],described, IBDA_DigitalDemodulatorInterface, bdaiface/IBDA_DigitalDemodulator, mstv.ibda_digitaldemodulator
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
 - IBDA_DigitalDemodulator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_DigitalDemodulator interface


## -description



The <b>IBDA_DigitalDemodulator</b> interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal. A Network Provider calls these methods on the filter to provide the demodulator with the information it needs to acquire a particular signal. The Network Provider obtains these values from the <a href="https://msdn.microsoft.com/81ed8c43-311c-47b1-bb86-8e86877648f5">Locator</a> object associated with the tune request or tuning space.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DigitalDemodulator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_DigitalDemodulator</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd693294(v=VS.85).aspx">get_InnerFECMethod</a>
</td>
<td align="left" width="63%">
Retrieves the inner forward error correction method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693295(v=VS.85).aspx">get_InnerFECRate</a>
</td>
<td align="left" width="63%">
Retrieves the inner forward error correction rate being used on the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f00553f-c0b1-4ff5-9c92-fe3a1990ef20">get_ModulationType</a>
</td>
<td align="left" width="63%">
Retrieves the modulation type for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693297(v=VS.85).aspx">get_OuterFECMethod</a>
</td>
<td align="left" width="63%">
Retrieves the outer forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693298(v=VS.85).aspx">get_OuterFECRate</a>
</td>
<td align="left" width="63%">
Retrieves the outer forward error correction rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaab17e3-8070-4f70-a31c-cd130edf1a4a">get_SpectralInversion</a>
</td>
<td align="left" width="63%">
Retrieves the spectral inversion value for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693300(v=VS.85).aspx">get_SymbolRate</a>
</td>
<td align="left" width="63%">
Retrieves the symbol rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693301(v=VS.85).aspx">put_InnerFECMethod</a>
</td>
<td align="left" width="63%">
Specifies the inner forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693302(v=VS.85).aspx">put_InnerFECRate</a>
</td>
<td align="left" width="63%">
Specifies the inner forward error correction rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693303(v=VS.85).aspx">put_ModulationType</a>
</td>
<td align="left" width="63%">
Specifies the modulation type for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693304(v=VS.85).aspx">put_OuterFECMethod</a>
</td>
<td align="left" width="63%">
Specifies the outer forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693305(v=VS.85).aspx">put_OuterFECRate</a>
</td>
<td align="left" width="63%">
Specifies the outer forward error correction rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693306(v=VS.85).aspx">put_SpectralInversion</a>
</td>
<td align="left" width="63%">
Specifies the spectral inversion value for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693307(v=VS.85).aspx">put_SymbolRate</a>
</td>
<td align="left" width="63%">
Specifies the symbol rate for the signal.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DigitalDemodulator)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

