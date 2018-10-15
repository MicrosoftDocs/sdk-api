---
UID: NN:mfidl.IMFSensorProcessActivity
title: IMFSensorProcessActivity
author: windows-sdk-content
description: Represents the activity of a process associated with a sensor.
old-location: mf\imfsensorprocessactivity.htm
tech.root: medfound
ms.assetid: 833A24EA-11E0-47CF-A710-06E38A1FD50A
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFSensorProcessActivity, IMFSensorProcessActivity interface [Media Foundation], IMFSensorProcessActivity interface [Media Foundation],described, mf.imfsensorprocessactivity, mfidl/IMFSensorProcessActivity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorProcessActivity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorProcessActivity interface


## -description


Represents the activity of a process associated with a sensor.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorProcessActivity</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorProcessActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorProcessActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E4277F4B-8CBB-4910-991B-1234AFEB49B3">GetProcessId</a>
</td>
<td align="left" width="63%">
Gets the ID of the process with which the activity is associated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C13F0ED-B2A6-43AC-92AA-87BF995DEFD7">GetReportTime</a>
</td>
<td align="left" width="63%">
Gets the time associated with the sensor activity report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1881652A-005C-4EFB-B4ED-3BEAC35A460A">GetStreamingMode</a>
</td>
<td align="left" width="63%">
Gets the streaming mode of the sensor process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C8A99D4B-F3D5-41D2-A956-C147900F28ED">GetStreamingState</a>
</td>
<td align="left" width="63%">
Gets a value indicating whether the sensor is currently streaming.

</td>
</tr>
</table> 

