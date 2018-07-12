---
UID: NN:locationapi.IDefaultLocation
title: IDefaultLocation
author: windows-sdk-content
description: IDefaultLocation provides methods used to specify or retrieve the default location.
old-location: winlocation\idefaultlocation.htm
old-project: locationapi
ms.assetid: 408062c8-2fea-4734-a243-e4ed21b7b3c3
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IDefaultLocation, IDefaultLocation interface [WinLocation], IDefaultLocation interface [WinLocation],described, locationapi/IDefaultLocation, winlocation.idefaultlocation
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
 - IDefaultLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDefaultLocation interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

<b>IDefaultLocation</b> provides methods used to specify or retrieve the default location.
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDefaultLocation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDefaultLocation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7b52dd6e-cba5-4248-b1be-b34e47a029d5">GetReport</a>
</td>
<td align="left" width="63%">
Gets the report from the default location provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50355f93-e609-44d5-925a-2de7af1e0564">SetReport</a>
</td>
<td align="left" width="63%">
Sets the report that the default location provider returns.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  An application does not receive the expected location change event from <a href="https://msdn.microsoft.com/14353c8e-15f5-493b-9b49-139924f2397e">OnLocationChanged</a> if both of the following conditions are true. First, the application runs as a service, in the context of the LOCALSERVICE, SYSTEM, or NETWORKSERVICE user account. Second, the location change event results from changing the default location, either manually when the user selects <b>Default Location</b> in Control Panel, or programmatically when an application calls <b>IDefaultLocation::SetReport</b>.</div>
<div> </div>


