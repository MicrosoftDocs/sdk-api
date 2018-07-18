---
UID: NN:locationapi.ILocationReport
title: ILocationReport
author: windows-sdk-content
description: The parent interface for location reports.
old-location: winlocation\ilocationreport.htm
old-project: LocationAPI
ms.assetid: 6dc78c26-36b3-4545-b5ba-7f04f6e67706
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ILocationReport, ILocationReport interface [WinLocation], ILocationReport interface [WinLocation],described, locationapi/ILocationReport, winlocation.ilocationreport
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
 - ILocationReport
product: Windows
targetos: Windows
req.lib: 
req.dll: LocationAPI.dll
req.irql: 
req.product: GDI+ 1.1
---

# ILocationReport interface


## -description


<p class="CCE_Message">[The Win32 Location API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/fd40bf4a-c59a-43a4-ab01-c671a8a41731">Windows.Devices.Geolocation</a>
API.
]

The parent interface for location reports. 
   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocationReport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ILocationReport</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c75b2ce3-8c60-4e26-870f-2bec599ea3b8">GetSensorID</a>
</td>
<td align="left" width="63%">
Retrieves the ID of the sensor that generated the location report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3573b2e7-fa76-4819-894d-d1215dc625bc">GetTimestamp</a>
</td>
<td align="left" width="63%">
Retrieves the date and time when the report was generated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves a property value from the location report.

</td>
</tr>
</table> 

