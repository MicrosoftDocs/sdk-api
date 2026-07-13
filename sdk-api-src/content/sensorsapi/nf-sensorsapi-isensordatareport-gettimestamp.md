---
UID: NF:sensorsapi.ISensorDataReport.GetTimestamp
title: ISensorDataReport::GetTimestamp (sensorsapi.h)
description: Retrieves the time at which the data report was created.
helpviewer_keywords: ["GetTimestamp","GetTimestamp method","GetTimestamp method","ISensorDataReport interface","ISensorDataReport interface","GetTimestamp method","ISensorDataReport.GetTimestamp","ISensorDataReport::GetTimestamp","sensorsapi/ISensorDataReport::GetTimestamp","winsensors_com_ref.isensordatareport_gettimestamp"]
old-location: winsensors_com_ref\isensordatareport_gettimestamp.htm
tech.root: winsensors
ms.assetid: 3366bfb5-1132-4960-8a0e-49967310ade5
ms.date: 09/19/2025
ms.keywords: GetTimestamp, GetTimestamp method, GetTimestamp method,ISensorDataReport interface, ISensorDataReport interface,GetTimestamp method, ISensorDataReport.GetTimestamp, ISensorDataReport::GetTimestamp, sensorsapi/ISensorDataReport::GetTimestamp, winsensors_com_ref.isensordatareport_gettimestamp
req.header: sensorsapi.h
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
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISensorDataReport::GetTimestamp
 - sensorsapi/ISensorDataReport::GetTimestamp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorDataReport.GetTimestamp
---

# ISensorDataReport::GetTimestamp


## -description

> [!IMPORTANT]
> Use the [UWP Sensor API](/windows/uwp/devices-sensors/sensors) instead.
>
> The COM-based Sensor API is deprecated and should not be used in new applications. No additional features or enhancements are planned, and support will be limited.

Retrieves the time at which the data report was created.

## -parameters

### -param pTimeStamp [out]

Address of a <a href="/windows/win32/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> variable that receives the time stamp.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The sensor driver did not return a valid time stamp for the data report.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pTimeStamp.

</td>
</tr>
</table>

## -remarks

Time stamps use Universal Coordinated Time (UTC).

## -see-also

<a href="/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport">ISensorDataReport</a>