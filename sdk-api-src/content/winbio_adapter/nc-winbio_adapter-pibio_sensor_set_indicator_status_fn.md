---
UID: NC:winbio_adapter.PIBIO_SENSOR_SET_INDICATOR_STATUS_FN
title: PIBIO_SENSOR_SET_INDICATOR_STATUS_FN (winbio_adapter.h)
description: Toggles the sensor indicator on or off.helpviewer_keywords: ["PIBIO_SENSOR_SET_INDICATOR_STATUS_FN","PIBIO_SENSOR_SET_INDICATOR_STATUS_FN callback","SensorAdapterSetIndicatorStatus","SensorAdapterSetIndicatorStatus callback function [Windows Biometric Framework API]","secbiomet.sensoradaptersetindicatorstatus","winbio_adapter/SensorAdapterSetIndicatorStatus"]
old-location: secbiomet\sensoradaptersetindicatorstatus.htm
tech.root: SecBioMet
ms.assetid: a47815d0-934c-43d4-8f4a-5f57a1c9f278
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_SET_INDICATOR_STATUS_FN, PIBIO_SENSOR_SET_INDICATOR_STATUS_FN callback, SensorAdapterSetIndicatorStatus, SensorAdapterSetIndicatorStatus callback function [Windows Biometric Framework API], secbiomet.sensoradaptersetindicatorstatus, winbio_adapter/SensorAdapterSetIndicatorStatus
f1_keywords:
- winbio_adapter/SensorAdapterSetIndicatorStatus
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- SensorAdapterSetIndicatorStatus
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_SENSOR_SET_INDICATOR_STATUS_FN callback function


## -description


Called by the Windows Biometric Framework to toggle the sensor indicator on or off.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.



### -param IndicatorStatus [in]

A <b>WINBIO_INDICATOR_STATUS</b> value. This can be one of the following:

<ul>
<li>WINBIO_INDICATOR_ON</li>
<li>WINBIO_INDICATOR_OFF</li>
</ul>

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
The <i>Pipeline</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>IndicatorStatus</i> parameter is not correct

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DEVICE_FAILURE </b></dt>
</dl>
</td>
<td width="60%">
There was a hardware failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b> or the <b>SensorHandle</b> member is set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The sensor does not have an indicator.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn">SensorAdapterGetIndicatorStatus</a>
 

 

