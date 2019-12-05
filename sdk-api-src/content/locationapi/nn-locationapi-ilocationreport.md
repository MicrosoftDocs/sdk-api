---
UID: NN:locationapi.ILocationReport
title: ILocationReport (locationapi.h)
description: The parent interface for location reports.
old-location: winlocation\ilocationreport.htm
tech.root: locationapi
ms.assetid: 6dc78c26-36b3-4545-b5ba-7f04f6e67706
ms.date: 12/05/2018
ms.keywords: ILocationReport, ILocationReport interface [WinLocation], ILocationReport interface [WinLocation],described, locationapi/ILocationReport, winlocation.ilocationreport
ms.topic: interface
f1_keywords:
- locationapi/ILocationReport
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
- ILocationReport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocationReport interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

The parent interface for location reports. 
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocationReport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILocationReport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocationReport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocationreport-getsensorid">GetSensorID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the sensor that generated the location report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocationreport-gettimestamp">GetTimestamp</a>
</td>
<td align="left" width="63%">
Retrieves the date and time when the report was generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocationreport-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the location report.

</td>
</tr>
</table> 

