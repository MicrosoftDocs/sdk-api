---
UID: NN:mfidl.IMFSensorActivityReport
title: IMFSensorActivityReport (mfidl.h)
author: windows-sdk-content
description: Represents an activity report for a sensor.
old-location: mf\imfsensoractivityreport.htm
tech.root: medfound
ms.assetid: 06612B8E-5C1E-487C-B6EF-15F65DEA27D0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSensorActivityReport, IMFSensorActivityReport interface [Media Foundation], IMFSensorActivityReport interface [Media Foundation],described, mf.imfsensoractivityreport, mfidl/IMFSensorActivityReport
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFSensorActivityReport"
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
 - IMFSensorActivityReport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorActivityReport interface


## -description


Represents an activity report for a sensor.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSensorActivityReport</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSensorActivityReport</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivityreport-getfriendlyname">GetFriendlyName</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the sensor associated with the report.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivityreport-getprocessactivity">GetProcessActivity</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a> object representing the current process activity of a sensor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivityreport-getprocesscount">GetProcessCount</a>
</td>
<td align="left" width="63%">
Gets the count of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a> objects, representing the current activity of a process associated with the sensor, that are available to be retrieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfsensoractivityreport-getsymboliclink">GetSymbolicLink</a>
</td>
<td align="left" width="63%">
Gets the symbolic link for the sensor associated with the report.

</td>
</tr>
</table> 

