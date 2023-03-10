---
UID: NC:winbio_adapter.PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN
title: PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN (winbio_adapter.h)
description: Notifies the sensor adapter that a particular calibration data format has been selected by the engine adapter.
helpviewer_keywords: ["PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN","PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN callback","SensorAdapterSetCalibrationFormat","SensorAdapterSetCalibrationFormat callback function [Windows Biometric Framework API]","secbiomet.sensoradaptersetcalibrationformat","winbio_adapter/SensorAdapterSetCalibrationFormat"]
old-location: secbiomet\sensoradaptersetcalibrationformat.htm
tech.root: SecBioMet
ms.assetid: 06BC3CBF-AB51-47C8-BCFB-ADC3D920F27B
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN, PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN callback, SensorAdapterSetCalibrationFormat, SensorAdapterSetCalibrationFormat callback function [Windows Biometric Framework API], secbiomet.sensoradaptersetcalibrationformat, winbio_adapter/SensorAdapterSetCalibrationFormat
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN
 - winbio_adapter/PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN
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
 - SensorAdapterSetCalibrationFormat
---

# PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN callback function


## -description

Called by the Windows Biometric Framework to notify the sensor adapter that a particular calibration data format has been selected by the engine adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Format [in]

Address of a <a href="/windows-hardware/drivers/ddi/content/winbio_ioctl/ns-winbio_ioctl-_winbio_capture_parameters">WINBIO_UUID</a> identifying the calibration data format selected by the Engine Adapter.

## -returns

The function will return one of the following <b>HRESULT</b> values. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK </b></dt>
</dl>
</td>
<td width="60%">
The operation succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL </b></dt>
</dl>
</td>
<td width="60%">
The Sensor Adapter doesn’t support dynamic calibration. This is only treated as an error if the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn">SensorAdapterQueryCalibrationFormats</a> method has previously indicated that the adapter supports dynamic calibration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_UNSUPPORTED_SENSOR_CALIBRATION_FORMAT </b></dt>
</dl>
</td>
<td width="60%">
The UUID specified in the <i>Format</i> parameter is not one of the ones supported by the Sensor Adapter. This error code will cause the Biometric Service to log the error and abort the configuration of the biometric unit.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_other_error </b></dt>
</dl>
</td>
<td width="60%">
Any other error code will cause the Biometric Service to log the error and abort the configuration of the biometric unit.

</td>
</tr>
</table>

## -remarks

The Sensor Adapter should store a copy of this UUID value for later use in interpreting the contents of any calibration buffers sent to its <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn">SensorAdapterAcceptCalibrationData</a> method.