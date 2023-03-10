---
UID: NC:winbio_adapter.PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN
title: PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN (winbio_adapter.h)
description: Determines the set of calibration formats supported by the Sensor Adapter.
helpviewer_keywords: ["PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN","PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN callback","SensorAdapterQueryCalibrationFormats","SensorAdapterQueryCalibrationFormats callback function [Windows Biometric Framework API]","secbiomet.sensoradapterquerycalibrationformats","winbio_adapter/SensorAdapterQueryCalibrationFormats"]
old-location: secbiomet\sensoradapterquerycalibrationformats.htm
tech.root: SecBioMet
ms.assetid: F8C97013-3BDA-445F-A2C2-60D08DD9C71A
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN, PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN callback, SensorAdapterQueryCalibrationFormats, SensorAdapterQueryCalibrationFormats callback function [Windows Biometric Framework API], secbiomet.sensoradapterquerycalibrationformats, winbio_adapter/SensorAdapterQueryCalibrationFormats
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
 - PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN
 - winbio_adapter/PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN
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
 - SensorAdapterQueryCalibrationFormats
---

# PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN callback function


## -description

Called by the Windows Biometric Framework to determine the set of calibration formats supported by the Sensor Adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param FormatArray [out]

Address of an array of empty <a href="/windows-hardware/drivers/ddi/content/winbio_ioctl/ns-winbio_ioctl-_winbio_capture_parameters">WINBIO_UUID</a> items. The <b>SensorAdapterQueryCalibrationFormats</b> method is expected to fill this array with one or more UUIDs identifying the calibration data formats known to the Sensor Adapter.

### -param FormatArraySize [in]

A value indicating the number of slots available in <i>FormatArray</i>. The <b>SensorAdapterQueryCalibrationFormats</b> method must not attempt to write more than this number of elements into <i>FormatArray</i>, or the results will be unpredictable.

### -param FormatCount [out]

Pointer to a variable that receives the number UUIDs returned in <i>FormatArray</i>. The <b>SensorAdapterQueryCalibrationFormats</b> method must set this value before returning.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL </b></dt>
</dl>
</td>
<td width="60%">
– The Sensor Adapter doesn’t support dynamic calibration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_other_error </b></dt>
</dl>
</td>
<td width="60%">
Any other error code will cause the Windows Biometric Framework to log the error and abort the configuration of the biometric unit.

</td>
</tr>
</table>

## -remarks

This method is called once during the initial configuration of a biometric unit.

Each calibration format supported by the Sensor Adapter is identified by a separate UUID value.

This method executes in the context of an arbitrary RPC server thread.

If the Sensor Adapter doesn’t support dynamic calibration, it should return a value of <b>E_NOTIMPL</b>. The Windows Biometric Framework will not treat this as an error unless the Engine Adapter requires dynamic calibration. (For details, see the description of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn">EngineAdapterSelectCalibrationFormat</a> method.)

If this method returns a value of <b>S_OK</b>, <i>FormatArray</i> and <i>FormatCount</i> must be set. It is an error for this method to return <b>S_OK</b> along with a zero value for <i>FormatCount</i>. Doing so will cause the Windows Biometric Framework to log a <b>WINBIO_E_INVALID_CALIBRATION_FORMAT_ARRAY</b> error message and abort the configuration of the biometric unit.