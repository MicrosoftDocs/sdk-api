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



