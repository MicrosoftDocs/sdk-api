---
UID: NN:locationapi.ILatLongReport
title: ILatLongReport (locationapi.h)
description: ILatLongReport represents a location report that contains information in the form of latitude and longitude.
old-location: winlocation\ilatlongreport.htm
tech.root: locationapi
ms.assetid: b489959e-74c7-46df-b63f-7d37e3a244d5
ms.date: 12/05/2018
ms.keywords: ILatLongReport, ILatLongReport interface [WinLocation], ILatLongReport interface [WinLocation],described, locationapi/ILatLongReport, winlocation.ilatlongreport
f1_keywords:
- locationapi/ILatLongReport
dev_langs:
- c++
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: LocationAPI.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- LocationAPI.dll
api_name:
- ILatLongReport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILatLongReport interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

<b>ILatLongReport</b> represents a location report that contains information in the form of latitude and longitude.
    
   
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILatLongReport</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a>. <b>ILatLongReport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILatLongReport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilatlongreport-getaltitude">GetAltitude</a>
</td>
<td align="left" width="63%">
Retrieves the altitude, in meters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilatlongreport-getaltitudeerror">GetAltitudeError</a>
</td>
<td align="left" width="63%">
Retrieves the altitude error, in meters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilatlongreport-geterrorradius">GetErrorRadius</a>
</td>
<td align="left" width="63%">
Retrieves a distance from the reported location, in meters. Combined with the location reported as the origin, this radius describes a circle in which the actual location is probably located.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilatlongreport-getlatitude">GetLatitude</a>
</td>
<td align="left" width="63%">
Retrieves the latitude.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilatlongreport-getlongitude">GetLongitude</a>
</td>
<td align="left" width="63%">
Retrieves the longitude.

</td>
</tr>
</table> 

