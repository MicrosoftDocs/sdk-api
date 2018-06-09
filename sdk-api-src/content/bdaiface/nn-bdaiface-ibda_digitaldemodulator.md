---
UID: NN:bdaiface.IBDA_DigitalDemodulator
title: IBDA_DigitalDemodulator
author: windows-sdk-content
description: The IBDA_DigitalDemodulator interface is exposed on BDA device filters, specifically demodulators, that are not capable of automatically detecting the characteristics of a signal.
old-location: mstv\ibda_digitaldemodulator.htm
old-project: mstv
ms.assetid: 13ecd348-dc2b-4e80-9875-927f4ed55c95
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IBDA_DigitalDemodulator, IBDA_DigitalDemodulator interface [Microsoft TV Technologies], IBDA_DigitalDemodulator interface [Microsoft TV Technologies],described, IBDA_DigitalDemodulatorInterface, bdaiface/IBDA_DigitalDemodulator, mstv.ibda_digitaldemodulator
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
 - IBDA_DigitalDemodulator
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
<a href="https://msdn.microsoft.com/a245c9fa-6f1e-4aa6-a5bf-b9707244a9e2">get_InnerFECMethod</a>
</td>
<td align="left" width="63%">
Retrieves the inner forward error correction method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56fb0c34-8c28-4eff-a1dd-d82c31b0e430">get_InnerFECRate</a>
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
<a href="https://msdn.microsoft.com/6fbedcba-4b76-4cf0-8fa1-c71140d49643">get_OuterFECMethod</a>
</td>
<td align="left" width="63%">
Retrieves the outer forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99f6e920-0b2d-4509-9a68-c6404d676b8a">get_OuterFECRate</a>
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
<a href="https://msdn.microsoft.com/d3640389-2533-4e6f-bc3e-7dceef76866b">get_SymbolRate</a>
</td>
<td align="left" width="63%">
Retrieves the symbol rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/618074c0-5139-4373-8bcd-9a8fd90a4ed7">put_InnerFECMethod</a>
</td>
<td align="left" width="63%">
Specifies the inner forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e87dbce2-6970-45f6-b08c-bddebeb4d1ca">put_InnerFECRate</a>
</td>
<td align="left" width="63%">
Specifies the inner forward error correction rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e2bf33f-b139-4455-ad49-c75e52f31083">put_ModulationType</a>
</td>
<td align="left" width="63%">
Specifies the modulation type for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ec9c75b-5f71-4a07-8234-8f38b96b962d">put_OuterFECMethod</a>
</td>
<td align="left" width="63%">
Specifies the outer forward error correction method for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60c35bd1-b971-411b-92bf-bbed41fc984c">put_OuterFECRate</a>
</td>
<td align="left" width="63%">
Specifies the outer forward error correction rate for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aabb829-5198-407f-a8f7-f99f87229560">put_SpectralInversion</a>
</td>
<td align="left" width="63%">
Specifies the spectral inversion value for the signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec37e7a5-d2e8-468a-8b5b-d1a1fa538bfe">put_SymbolRate</a>
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
 

 

