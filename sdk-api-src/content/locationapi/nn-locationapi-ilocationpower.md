---
UID: NN:locationapi.ILocationPower
title: ILocationPower (locationapi.h)
author: windows-sdk-content
description: Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).
old-location: winlocation\ilocationpower.htm
tech.root: locationapi
ms.assetid: bf0a0c13-a50f-4ed8-bc29-7d70561da306
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILocationPower, ILocationPower interface [WinLocation], ILocationPower interface [WinLocation],described, locationapi/ILocationPower, winlocation.ilocationpower
ms.topic: interface
f1_keywords: 
 - "locationapi/ILocationPower"
req.header: locationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: LocationApi.idl
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
 - ILocationPower
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocationPower interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.devices.geolocation">Windows.Devices.Geolocation</a>API.
]

Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).

Most apps will not need to use this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocationPower</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILocationPower</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocationPower</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-connect-vb">Connect</a>
</td>
<td align="left" width="63%">
Notify the location platform that an app has connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxserver-disconnect-vb">Disconnect</a>
</td>
<td align="left" width="63%">
Notify the location platform that an app has disconnected.

</td>
</tr>
</table> 

