---
UID: NN:locationapi.ILocation
title: ILocation
author: windows-sdk-content
description: Provides methods used to manage location reports, event registration, and sensor permissions.
old-location: winlocation\ilocation.htm
old-project: LocationAPI
ms.assetid: beeedbbd-df93-4c05-a215-4cfd14e03076
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ILocation, ILocation interface [WinLocation], ILocation interface [WinLocation],described, locationapi/ILocation, winlocation.ilocation
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
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - LocationAPI.dll
api_name:
 - ILocation
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocation interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Provides methods used to manage location reports, event registration, and sensor permissions.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILocation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/caa34e34-7370-4e42-9c0f-00498f5fc37d">GetDesiredAccuracy</a>
</td>
<td align="left" width="63%">
Retrieves the current requested accuracy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69d0fed5-7f02-4d74-bdbd-3a0fd85e76ed">GetReport</a>
</td>
<td align="left" width="63%">
Retrieves a location report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7bcd665-317c-428a-aa20-0d09c8d7a813">GetReportInterval</a>
</td>
<td align="left" width="63%">
Retrieves the minimum amount of time, in milliseconds, between report events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b7c72cc-fa09-44b2-97be-f200fab7b31d">GetReportStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status for the specified report type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1aca3e5b-20cb-4fa9-b28d-7d992601df96">RegisterForReport</a>
</td>
<td align="left" width="63%">
Requests location report events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eef60203-8705-4f68-be30-c9e7938e5596">RequestPermissions</a>
</td>
<td align="left" width="63%">
Opens a system dialog box to request user permission for location-enabled devices.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85623570-3b48-42ea-babd-fe4282629d92">SetDesiredAccuracy</a>
</td>
<td align="left" width="63%">
Specifies the requested accuracy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b48f64d-47e8-41cc-a7a1-970654896e7e">SetReportInterval</a>
</td>
<td align="left" width="63%">
Specifies the minimum amount of time, in milliseconds, between report events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/333bd127-2c6a-4f09-9f86-4f8e68a9ea55">UnregisterForReport</a>
</td>
<td align="left" width="63%">
Stops event notifications for the specified report type.

</td>
</tr>
</table> 


## -remarks



When <b>CoCreateInstance</b> is callled to create an <b>ILocation</b> object, it may result in a notification being displayed in the taskbar, and a Location Activity event being logged in Event Viewer, if it is the application's first use of location.



