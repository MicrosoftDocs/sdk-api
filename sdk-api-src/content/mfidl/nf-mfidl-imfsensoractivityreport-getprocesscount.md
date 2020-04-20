---
UID: NF:mfidl.IMFSensorActivityReport.GetProcessCount
title: IMFSensorActivityReport::GetProcessCount (mfidl.h)
description: Gets the count of IMFSensorProcessActivity objects, representing the current activity of a process associated with the sensor, that are available to be retrieved.helpviewer_keywords: ["GetProcessCount","GetProcessCount method [Media Foundation]","GetProcessCount method [Media Foundation]","IMFSensorActivityReport interface","IMFSensorActivityReport interface [Media Foundation]","GetProcessCount method","IMFSensorActivityReport.GetProcessCount","IMFSensorActivityReport::GetProcessCount","mf.imfsensoractivityreport_getprocesscount","mfidl/IMFSensorActivityReport::GetProcessCount"]
old-location: mf\imfsensoractivityreport_getprocesscount.htm
tech.root: medfound
ms.assetid: 9C3DAB31-9D28-42CB-AFB8-6288658FF6B0
ms.date: 12/05/2018
ms.keywords: GetProcessCount, GetProcessCount method [Media Foundation], GetProcessCount method [Media Foundation],IMFSensorActivityReport interface, IMFSensorActivityReport interface [Media Foundation],GetProcessCount method, IMFSensorActivityReport.GetProcessCount, IMFSensorActivityReport::GetProcessCount, mf.imfsensoractivityreport_getprocesscount, mfidl/IMFSensorActivityReport::GetProcessCount
f1_keywords:
- mfidl/IMFSensorActivityReport.GetProcessCount
dev_langs:
- c++
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
- IMFSensorActivityReport.GetProcessCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSensorActivityReport::GetProcessCount


## -description


Gets the count of <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity">IMFSensorProcessActivity</a> objects, representing the current activity of a process associated with the sensor, that are available to be retrieved.


## -parameters




### -param pcCount [out]

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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport">IMFSensorActivityReport</a>
 

 

