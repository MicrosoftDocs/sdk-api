---
UID: NN:locationapi.ICivicAddressReport
title: ICivicAddressReport
author: windows-sdk-content
description: ICivicAddressReport represents a location report that contains information in the form of a street address.
old-location: winlocation\icivicaddressreport.htm
old-project: LocationAPI
ms.assetid: ba8c66cb-be94-4649-ada9-620ed3b35516
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ICivicAddressReport, ICivicAddressReport interface [WinLocation], ICivicAddressReport interface [WinLocation],described, locationapi/ICivicAddressReport, winlocation.icivicaddressreport
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
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	LocationAPI.dll
api_name:
-	ICivicAddressReport
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ICivicAddressReport interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

<b>ICivicAddressReport</b> represents a location report that contains information in the form of a street address.
    
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICivicAddressReport</b> interface inherits from <a href="https://msdn.microsoft.com/6dc78c26-36b3-4545-b5ba-7f04f6e67706">ILocationReport</a>. <b>ICivicAddressReport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/946f0e69-7139-45e9-8da4-755225ce1bd1">GetAddressLine1</a>
</td>
<td align="left" width="63%">
Retrieves the first line of a street address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c66b294-15a9-490a-b77c-ff48f35d1d3b">GetAddressLine2</a>
</td>
<td align="left" width="63%">
Retrieves the second line of a street address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c87debb3-63ab-4d5b-85ff-0ee0653d6ffe">GetCity</a>
</td>
<td align="left" width="63%">
Retrieves the city name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1bcf7939-e047-412f-874d-18bb5e93e5ec">GetCountryRegion</a>
</td>
<td align="left" width="63%">
Retrieves the country or region name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec32dee1-e9ce-40a0-bca0-6f5f767b7604">GetDetailLevel</a>
</td>
<td align="left" width="63%">
Retrieves a value that indicates the level of detail provided by the civic address report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1580a1b9-1503-43d8-af1c-3b2ba8e9f81a">GetPostalCode</a>
</td>
<td align="left" width="63%">
Retrieves the postal code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f47670c-5549-46af-8a16-0e9a43cf90aa">GetStateProvince</a>
</td>
<td align="left" width="63%">
Retrieves the state or province name.

</td>
</tr>
</table> 


## -remarks



Note that any property value can be <b>NULL</b> if the value is not available.



