---
UID: NN:locationapi.IDefaultLocation
title: IDefaultLocation (locationapi.h)
author: windows-sdk-content
description: IDefaultLocation provides methods used to specify or retrieve the default location.
old-location: winlocation\idefaultlocation.htm
tech.root: locationapi
ms.assetid: 408062c8-2fea-4734-a243-e4ed21b7b3c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDefaultLocation, IDefaultLocation interface [WinLocation], IDefaultLocation interface [WinLocation],described, locationapi/IDefaultLocation, winlocation.idefaultlocation
ms.topic: interface
f1_keywords: 
 - "locationapi/IDefaultLocation"
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
 - IDefaultLocation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDefaultLocation interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

<b>IDefaultLocation</b> provides methods used to specify or retrieve the default location.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDefaultLocation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDefaultLocation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDefaultLocation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-idefaultlocation-getreport">GetReport</a>
</td>
<td align="left" width="63%">
Gets the report from the default location provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-idefaultlocation-setreport">SetReport</a>
</td>
<td align="left" width="63%">
Sets the report that the default location provider returns.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  An application does not receive the expected location change event from <a href="https://docs.microsoft.com/windows/desktop/api/locationapi/nf-locationapi-ilocationevents-onlocationchanged">OnLocationChanged</a> if both of the following conditions are true. First, the application runs as a service, in the context of the LOCALSERVICE, SYSTEM, or NETWORKSERVICE user account. Second, the location change event results from changing the default location, either manually when the user selects <b>Default Location</b> in Control Panel, or programmatically when an application calls <b>IDefaultLocation::SetReport</b>.</div>
<div> </div>


