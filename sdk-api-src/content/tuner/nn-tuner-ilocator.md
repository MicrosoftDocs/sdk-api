---
UID: NN:tuner.ILocator
title: ILocator (tuner.h)
author: windows-sdk-content
description: The ILocator interface is implemented (through derived interfaces such as IATSCLocator) on Locator objects that contain tuning information about the tuning space.
old-location: mstv\ilocator.htm
tech.root: mstv
ms.assetid: 1d6c18f0-e7f1-4a1c-9edb-e4b66297becf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILocator, ILocator interface [Microsoft TV Technologies], ILocator interface [Microsoft TV Technologies],described, ILocatorInterface, mstv.ilocator, tuner/ILocator
ms.topic: interface
f1_keywords: ["tuner/ILocator"]
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
 - ILocator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocator interface


## -description



The <b>ILocator</b> interface is implemented (through derived interfaces such as <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator</a>) on Locator objects that contain tuning information about the tuning space. This base interface is never used directly, but only through the derived interfaces that are specific for a given network type.

 Locator objects can be created dynamically by Guide Store Loaders that have the necessary information about the tuning space, or a default locator for a tuning space can be installed by the third party who installs the tuning space. In any case, applications never create or examine locators except in certain testing or debugging scenarios. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocator</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ILocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the Locator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_carrierfrequency">get_CarrierFrequency</a>
</td>
<td align="left" width="63%">
Gets the frequency of the RF signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_innerfec">get_InnerFEC</a>
</td>
<td align="left" width="63%">
Gets the type of inner forward error correction (FEC) that is used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_innerfecrate">get_InnerFECRate</a>
</td>
<td align="left" width="63%">
Gets the inner FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_modulation">get_Modulation</a>
</td>
<td align="left" width="63%">
Gets the modulation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_outerfec">get_OuterFEC</a>
</td>
<td align="left" width="63%">
Gets the type of outer FEC that is used.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_outerfecrate">get_OuterFECRate</a>
</td>
<td align="left" width="63%">
Gets the outer FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-get_symbolrate">get_SymbolRate</a>
</td>
<td align="left" width="63%">
Gets the quadrature phase-shift keying (QPSK) symbol rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_carrierfrequency">put_CarrierFrequency</a>
</td>
<td align="left" width="63%">
Sets the frequency of the RF signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_innerfec">put_InnerFEC</a>
</td>
<td align="left" width="63%">
Sets the type of inner FEC to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_innerfecrate">put_InnerFECRate</a>
</td>
<td align="left" width="63%">
Sets the inner FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_modulation">put_Modulation</a>
</td>
<td align="left" width="63%">
Sets the modulation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_outerfec">put_OuterFEC</a>
</td>
<td align="left" width="63%">
Sets the type of outer FEC to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_outerfecrate">put_OuterFECRate</a>
</td>
<td align="left" width="63%">
Sets the outer FEC rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilocator-put_symbolrate">put_SymbolRate</a>
</td>
<td align="left" width="63%">
Sets the QPSK symbol rate.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ILocator)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

