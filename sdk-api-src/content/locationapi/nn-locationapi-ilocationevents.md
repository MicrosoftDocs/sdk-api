---
UID: NN:locationapi.ILocationEvents
title: ILocationEvents
author: windows-sdk-content
description: ILocationEvents provides callback methods that you must implement if you want to receive event notifications.
old-location: winlocation\ilocationevents.htm
old-project: LocationAPI
ms.assetid: 5281ae0f-8599-4f84-a3f3-cde8c69e893d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: ILocationEvents, ILocationEvents interface [WinLocation], ILocationEvents interface [WinLocation],described, locationapi/ILocationEvents, winlocation.ilocationevents
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
 - ILocationEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocationEvents interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

<b>ILocationEvents</b> provides callback methods that 
    you must implement if you want to receive event notifications.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocationEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILocationEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocationEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14353c8e-15f5-493b-9b49-139924f2397e">OnLocationChanged</a>
</td>
<td align="left" width="63%">
Called when a new location report is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d13d8b72-3188-479f-a70c-52b1a9435b80">OnStatusChanged</a>
</td>
<td align="left" width="63%">
Called when a report status changes.

</td>
</tr>
</table> 

