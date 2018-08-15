---
UID: NF:mfidl.IMFSensorActivityReport.GetProcessCount
title: IMFSensorActivityReport::GetProcessCount
author: windows-sdk-content
description: Gets the count of IMFSensorProcessActivity objects, representing the current activity of a process associated with the sensor, that are available to be retrieved.
old-location: mf\imfsensoractivityreport_getprocesscount.htm
old-project: medfound
ms.assetid: 9C3DAB31-9D28-42CB-AFB8-6288658FF6B0
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetProcessCount, GetProcessCount method [Media Foundation], GetProcessCount method [Media Foundation],IMFSensorActivityReport interface, IMFSensorActivityReport interface [Media Foundation],GetProcessCount method, IMFSensorActivityReport.GetProcessCount, IMFSensorActivityReport::GetProcessCount, mf.imfsensoractivityreport_getprocesscount, mfidl/IMFSensorActivityReport::GetProcessCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
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
 - IMFSensorActivityReport.GetProcessCount
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorActivityReport::GetProcessCount


## -description


Gets the count of <a href="https://msdn.microsoft.com/833A24EA-11E0-47CF-A710-06E38A1FD50A">IMFSensorProcessActivity</a> objects, representing the current activity of a process associated with the sensor, that are available to be retrieved.


## -parameters




### -param pcCount






#### - pulCount [out]

A pointer in which the process count is stored.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pulCount</i> parameter is null.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/06612B8E-5C1E-487C-B6EF-15F65DEA27D0">IMFSensorActivityReport</a>
 

 

