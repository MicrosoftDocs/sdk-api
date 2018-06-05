---
UID: NC:winbio_adapter.PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN
title: PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN
author: windows-sdk-content
description: Determines the set of calibration formats supported by the Sensor Adapter.
old-location: secbiomet\sensoradapterquerycalibrationformats.htm
old-project: SecBioMet
ms.assetid: F8C97013-3BDA-445F-A2C2-60D08DD9C71A
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN, PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN callback, SensorAdapterQueryCalibrationFormats, SensorAdapterQueryCalibrationFormats callback function [Windows Biometric Framework API], secbiomet.sensoradapterquerycalibrationformats, winbio_adapter/SensorAdapterQueryCalibrationFormats
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	SensorAdapterQueryCalibrationFormats
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_QUERY_CALIBRATION_FORMATS_FN callback function


## -description


Called by the Windows Biometric Framework to determine the set of calibration formats supported by the Sensor Adapter.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param FormatArray [out]

Address of an array of empty <a href="https://msdn.microsoft.com/library/windows/hardware/ff536480">WINBIO_UUID</a> items. The <b>SensorAdapterQueryCalibrationFormats</b> method is expected to fill this array with one or more UUIDs identifying the calibration data formats known to the Sensor Adapter.


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

If the Sensor Adapter doesn’t support dynamic calibration, it should return a value of <b>E_NOTIMPL</b>. The Windows Biometric Framework will not treat this as an error unless the Engine Adapter requires dynamic calibration. (For details, see the description of the <a href="https://msdn.microsoft.com/1B4920D9-3C8E-4206-A71B-619A14ADD10A">EngineAdapterSelectCalibrationFormat</a> method.)

If this method returns a value of <b>S_OK</b>, <i>FormatArray</i> and <i>FormatCount</i> must be set. It is an error for this method to return<b>S_OK</b> along with a zero value for <i>FormatCount</i>. Doing so will cause the Windows Biometric Framework to log a <b>WINBIO_E_INVALID_CALIBRATION_FORMAT_ARRAY</b> error message and abort the configuration of the biometric unit.



