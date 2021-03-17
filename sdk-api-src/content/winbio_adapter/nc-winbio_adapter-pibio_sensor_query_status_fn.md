---
UID: NC:winbio_adapter.PIBIO_SENSOR_QUERY_STATUS_FN
title: PIBIO_SENSOR_QUERY_STATUS_FN (winbio_adapter.h)
description: Retrieves information about the current status of the sensor device.
helpviewer_keywords: ["PIBIO_SENSOR_QUERY_STATUS_FN","PIBIO_SENSOR_QUERY_STATUS_FN callback","SensorAdapterQueryStatus","SensorAdapterQueryStatus callback function [Windows Biometric Framework API]","secbiomet.sensoradapterquerystatus","winbio_adapter/SensorAdapterQueryStatus"]
old-location: secbiomet\sensoradapterquerystatus.htm
tech.root: SecBioMet
ms.assetid: 88c22183-5bc8-4ac9-9048-72ee7a861b76
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_QUERY_STATUS_FN, PIBIO_SENSOR_QUERY_STATUS_FN callback, SensorAdapterQueryStatus, SensorAdapterQueryStatus callback function [Windows Biometric Framework API], secbiomet.sensoradapterquerystatus, winbio_adapter/SensorAdapterQueryStatus
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_SENSOR_QUERY_STATUS_FN
 - winbio_adapter/PIBIO_SENSOR_QUERY_STATUS_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - SensorAdapterQueryStatus
---

# PIBIO_SENSOR_QUERY_STATUS_FN callback function


## -description

Called by the Windows Biometric Framework to retrieve information about the current status of the sensor device.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Status [out]

Pointer to a WINBIO_SENSOR_STATUS value that receives the status information.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b> or the <b>SensorHandle</b> member is set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>