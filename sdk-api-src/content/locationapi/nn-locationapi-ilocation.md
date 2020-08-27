---
UID: NN:locationapi.ILocation
title: ILocation (locationapi.h)
description: Provides methods used to manage location reports, event registration, and sensor permissions.
helpviewer_keywords: ["ILocation","ILocation interface [WinLocation]","ILocation interface [WinLocation]","described","locationapi/ILocation","winlocation.ilocation"]
old-location: winlocation\ilocation.htm
tech.root: winlocation
ms.assetid: beeedbbd-df93-4c05-a215-4cfd14e03076
ms.date: 12/05/2018
ms.keywords: ILocation, ILocation interface [WinLocation], ILocation interface [WinLocation],described, locationapi/ILocation, winlocation.ilocation
f1_keywords:
- locationapi/ILocation
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
- ILocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocation interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

Provides methods used to manage location reports, event registration, and sensor permissions.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILocation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-getdesiredaccuracy">GetDesiredAccuracy</a>
</td>
<td align="left" width="63%">
Retrieves the current requested accuracy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreport">GetReport</a>
</td>
<td align="left" width="63%">
Retrieves a location report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportinterval">GetReportInterval</a>
</td>
<td align="left" width="63%">
Retrieves the minimum amount of time, in milliseconds, between report events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-getreportstatus">GetReportStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status for the specified report type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-registerforreport">RegisterForReport</a>
</td>
<td align="left" width="63%">
Requests location report events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-requestpermissions">RequestPermissions</a>
</td>
<td align="left" width="63%">
Opens a system dialog box to request user permission for location-enabled devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-setdesiredaccuracy">SetDesiredAccuracy</a>
</td>
<td align="left" width="63%">
Specifies the requested accuracy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-setreportinterval">SetReportInterval</a>
</td>
<td align="left" width="63%">
Specifies the minimum amount of time, in milliseconds, between report events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocation-unregisterforreport">UnregisterForReport</a>
</td>
<td align="left" width="63%">
Stops event notifications for the specified report type.

</td>
</tr>
</table> 


## -remarks



When <b>CoCreateInstance</b> is callled to create an <b>ILocation</b> object, it may result in a notification being displayed in the taskbar, and a Location Activity event being logged in Event Viewer, if it is the application's first use of location.



