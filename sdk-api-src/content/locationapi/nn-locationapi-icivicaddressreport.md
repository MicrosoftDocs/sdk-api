---
UID: NN:locationapi.ICivicAddressReport
title: ICivicAddressReport (locationapi.h)
author: windows-sdk-content
description: ICivicAddressReport represents a location report that contains information in the form of a street address.
old-location: winlocation\icivicaddressreport.htm
tech.root: locationapi
ms.assetid: ba8c66cb-be94-4649-ada9-620ed3b35516
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICivicAddressReport, ICivicAddressReport interface [WinLocation], ICivicAddressReport interface [WinLocation],described, locationapi/ICivicAddressReport, winlocation.icivicaddressreport
ms.topic: interface
f1_keywords: ["locationapi/ICivicAddressReport"]
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
 - ICivicAddressReport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICivicAddressReport interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

<b>ICivicAddressReport</b> represents a location report that contains information in the form of a street address.
    
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICivicAddressReport</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nn-locationapi-ilocationreport">ILocationReport</a>. <b>ICivicAddressReport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICivicAddressReport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getaddressline1">GetAddressLine1</a>
</td>
<td align="left" width="63%">
Retrieves the first line of a street address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getaddressline2">GetAddressLine2</a>
</td>
<td align="left" width="63%">
Retrieves the second line of a street address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getcity">GetCity</a>
</td>
<td align="left" width="63%">
Retrieves the city name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getcountryregion">GetCountryRegion</a>
</td>
<td align="left" width="63%">
Retrieves the country or region name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getdetaillevel">GetDetailLevel</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the level of detail provided by the civic address report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getpostalcode">GetPostalCode</a>
</td>
<td align="left" width="63%">
Retrieves the postal code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-icivicaddressreport-getstateprovince">GetStateProvince</a>
</td>
<td align="left" width="63%">
Retrieves the state or province name.

</td>
</tr>
</table> 


## -remarks



Note that any property value can be <b>NULL</b> if the value is not available.



