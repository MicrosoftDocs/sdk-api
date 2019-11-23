---
UID: NN:tuner.IDVBSLocator
title: IDVBSLocator (tuner.h)

description: The IDVBSLocator interface is implemented on the DVBSLocator object.
old-location: mstv\idvbslocator.htm
tech.root: mstv
ms.assetid: a9f02e78-3800-4b14-81df-acab01ea072b

ms.date: 12/05/2018
ms.keywords: IDVBSLocator, IDVBSLocator interface [Microsoft TV Technologies], IDVBSLocator interface [Microsoft TV Technologies],described, IDVBSLocatorInterface, mstv.idvbslocator, tuner/IDVBSLocator
ms.topic: interface
f1_keywords: 
 - "tuner/IDVBSLocator"
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
 - IDVBSLocator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVBSLocator interface


## -description



The <b>IDVBSLocator</b> interface is implemented on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/dvbslocator-object">DVBSLocator</a> object. It provides information to enable a tuner to acquire a satellite DVB (DVB-S) transmission. The methods for acquiring a transport stream once the signal is tuned are provided by IDVBTuneRequest. Locator data is meant for consumption by the BDA hardware drivers. Applications do not need to interpret any of this data except perhaps for some debugging purposes.

Locators can be created dynamically when the tune request is created, by a loader that has access to the necessary information about the tuning space, or a default locator can be installed when the tuning space is first installed, and the loader can use the default locator when creating tune requests. Applications do not need to use any of the Locator interfaces unless they are creating tune requests. All Locator objects also support <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBSLocator</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>. <b>IDVBSLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBSLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-get_azimuth">get_Azimuth</a>
</td>
<td align="left" width="63%">
Retrieves the azimuth setting used for positioning the satellite dish.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-get_elevation">get_Elevation</a>
</td>
<td align="left" width="63%">
Retrieves the elevation of the satellite in tenths of a degree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-get_orbitalposition">get_OrbitalPosition</a>
</td>
<td align="left" width="63%">
Retrieves the setting for the satellite's orbital position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/polarisation">get_SignalPolarisation</a>
</td>
<td align="left" width="63%">
Retrieves the signal polarisation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-get_westposition">get_WestPosition</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the orbital position is given in east or west longitude.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-put_azimuth">put_Azimuth</a>
</td>
<td align="left" width="63%">
Adjusts the azimuth setting used for positioning the satellite dish.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-put_elevation">put_Elevation</a>
</td>
<td align="left" width="63%">
Sets the elevation of the satellite in tenths of a degree.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-put_orbitalposition">put_OrbitalPosition</a>
</td>
<td align="left" width="63%">
Sets the setting for the satellite's orbital position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-put_signalpolarisation">put_SignalPolarisation</a>
</td>
<td align="left" width="63%">
Sets the signal polarisation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbslocator-put_westposition">put_WestPosition</a>
</td>
<td align="left" width="63%">
Sets the longitudinal position as west longitude or east longitude.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBSLocator)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idigitallocator~r1">IDigitalLocator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

