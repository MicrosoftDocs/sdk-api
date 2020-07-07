---
UID: NN:tuner.IDVBTLocator
title: IDVBTLocator (tuner.h)
description: The IDVBTLocator interface is implemented on the DVBTLocator object.
helpviewer_keywords: ["IDVBTLocator","IDVBTLocator interface [Microsoft TV Technologies]","IDVBTLocator interface [Microsoft TV Technologies]","described","IDVBTLocatorInterface","mstv.idvbtlocator","tuner/IDVBTLocator"]
old-location: mstv\idvbtlocator.htm
tech.root: mstv
ms.assetid: f5a95a68-fee0-404c-b9c6-6b808977f8d2
ms.date: 12/05/2018
ms.keywords: IDVBTLocator, IDVBTLocator interface [Microsoft TV Technologies], IDVBTLocator interface [Microsoft TV Technologies],described, IDVBTLocatorInterface, mstv.idvbtlocator, tuner/IDVBTLocator
f1_keywords:
- tuner/IDVBTLocator
dev_langs:
- c++
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
- tuner.h
api_name:
- IDVBTLocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVBTLocator interface


## -description



The <b>IDVBTLocator</b> interface is implemented on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/dvbtlocator-object">DVBTLocator</a> object. It provides methods to enable a tuner to acquire a terrestrial DVB (DVB-T) transport stream. The data types are defined in Bdatypes.h. Locator data is meant for consumption by the BDA hardware drivers. Applications do not need to interpret any of this data except perhaps for some debugging purposes.

Locators can be created dynamically when the tune request is created, by a loader that has access to the necessary information about the tuning space, or a default locator can be installed when the tuning space is first installed, and the loader can use the default locator when creating tune requests. Applications do not need to use any of the Locator interfaces unless they are creating tune requests. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBTLocator</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>. <b>IDVBTLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBTLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_bandwidth">get_Bandwidth</a>
</td>
<td align="left" width="63%">
Retrieves the bandwidth of the frequency in megahertz, usually 7 or 8.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_guard">get_Guard</a>
</td>
<td align="left" width="63%">
Retrieves the guard interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_halpha">get_HAlpha</a>
</td>
<td align="left" width="63%">
Retrieves the hierarchy alpha.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_lpinnerfec">get_LPInnerFEC</a>
</td>
<td align="left" width="63%">
Retrieves the inner FEC type of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_lpinnerfecrate">get_LPInnerFECRate</a>
</td>
<td align="left" width="63%">
Retrieves the inner FEC rate of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_mode">get_Mode</a>
</td>
<td align="left" width="63%">
Receives the transmission mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-get_otherfrequencyinuse">get_OtherFrequencyInUse</a>
</td>
<td align="left" width="63%">
Indicates whether the frequency is being used by another DVB-T broadcaster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_bandwidth">put_Bandwidth</a>
</td>
<td align="left" width="63%">
Sets the bandwidth of the frequency in megahertz, usually 7 or 8.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_guard">put_Guard</a>
</td>
<td align="left" width="63%">
Sets the guard interval.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_halpha">put_HAlpha</a>
</td>
<td align="left" width="63%">
Sets the hierarchy alpha.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_lpinnerfec">put_LPInnerFEC</a>
</td>
<td align="left" width="63%">
Sets the inner FEC type of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_lpinnerfecrate">put_LPInnerFECRate</a>
</td>
<td align="left" width="63%">
Sets the inner FEC rate of the low-priority stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_mode">put_Mode</a>
</td>
<td align="left" width="63%">
Sets the transmission mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbtlocator-put_otherfrequencyinuse">put_OtherFrequencyInUse</a>
</td>
<td align="left" width="63%">
Specifies whether the frequency is being used by another DVB-T broadcaster.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBTLocator)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

