---
UID: NN:locationapi.ILocationPower
title: ILocationPower
author: windows-driver-content
description: Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).
old-location: winlocation\ilocationpower.htm
old-project: LocationAPI
ms.assetid: bf0a0c13-a50f-4ed8-bc29-7d70561da306
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ILocationPower, ILocationPower interface [WinLocation], ILocationPower interface [WinLocation],described, locationapi/ILocationPower, winlocation.ilocationpower
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	LocationAPI.dll
api_name:
-	ILocationPower
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocationPower interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

Used by Windows Store app browsers in Windows 8 to notify the location platform that an app has been suspended (disconnect) and restored (connect).

Most apps will not need to use this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocationPower</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILocationPower</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/6c0145e0-974e-42b2-936e-9396f5c96e72">Connect</a>
</td>
<td align="left" width="63%">
Notify the location platform that an app has connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bf9bc29-4e81-4d80-8de5-317678b34792">Disconnect</a>
</td>
<td align="left" width="63%">
Notify the location platform that an app has disconnected.

</td>
</tr>
</table> 

