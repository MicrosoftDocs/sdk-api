---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFSensorActivityReport interface


## -description


Represents an activity report for a sensor.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorActivityReport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFSensorActivityReport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSensorActivityReport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6E8D7039-9CBF-45A0-8CAE-48F79091D40B">GetActivityReport</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IMFSensorActivityReport</b> based on the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66FDBCE0-E3F3-43A4-B34A-7FE6C7F3F918">GetActivityReportByDeviceName</a>
</td>
<td align="left" width="63%">
Retrieves an <b>IMFSensorActivityReport</b> based on the specified device name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the count of <b>IMFSensorActivityReport</b> objects that are available to be retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406579">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the sensor associated with the report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9E18EC3-83E4-430B-B7A4-49FC9736A94E">GetProcessActivity</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a> object representing the current process activity of a sensor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9C3DAB31-9D28-42CB-AFB8-6288658FF6B0">GetProcessCount</a>
</td>
<td align="left" width="63%">
Gets the count of <a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a> objects, representing the current activity of a process associated with the sensor, that are available to be retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BF0BDB21-DE87-4177-A94F-8BA8FD571B02">GetSymbolicLink</a>
</td>
<td align="left" width="63%">
Gets the symbolic link for the sensor associated with the report.

</td>
</tr>
</table> 

