---
UID: NN:locationapi.ILatLongReport
title: ILatLongReport
author: windows-sdk-content
description: ILatLongReport represents a location report that contains information in the form of latitude and longitude.
old-location: winlocation\ilatlongreport.htm
old-project: locationapi
ms.assetid: b489959e-74c7-46df-b63f-7d37e3a244d5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ILatLongReport, ILatLongReport interface [WinLocation], ILatLongReport interface [WinLocation],described, locationapi/ILatLongReport, winlocation.ilatlongreport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: LOCATION_REPORT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILatLongReport
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILatLongReport interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>API.
]

<b>ILatLongReport</b> represents a location report that contains information in the form of latitude and longitude.
    
   
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILatLongReport</b> interface inherits from <a href="https://msdn.microsoft.com/6dc78c26-36b3-4545-b5ba-7f04f6e67706">ILocationReport</a>. <b>ILatLongReport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7ab8e3fb-03da-4529-aaf0-3a178474e4a5">GetAltitude</a>
</td>
<td align="left" width="63%">
Retrieves the altitude, in meters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/313aefda-785c-43ce-a71c-cacfd929e27e">GetAltitudeError</a>
</td>
<td align="left" width="63%">
Retrieves the altitude error, in meters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb0941da-607d-4082-ac8c-91d2edafa8ab">GetErrorRadius</a>
</td>
<td align="left" width="63%">
Retrieves a distance from the reported location, in meters. Combined with the location reported as the origin, this radius describes a circle in which the actual location is probably located.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81392683-61bc-4b17-8f3c-172b66bd543b">GetLatitude</a>
</td>
<td align="left" width="63%">
Retrieves the latitude.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77fa407b-109c-45aa-bbdb-0b8a40d222e5">GetLongitude</a>
</td>
<td align="left" width="63%">
Retrieves the longitude.

</td>
</tr>
</table> 

