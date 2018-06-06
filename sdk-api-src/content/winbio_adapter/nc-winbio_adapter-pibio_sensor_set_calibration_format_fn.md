---
UID: NC:winbio_adapter.PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN
title: PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN
author: windows-sdk-content
description: Notifies the sensor adapter that a particular calibration data format has been selected by the engine adapter.
old-location: secbiomet\sensoradaptersetcalibrationformat.htm
old-project: SecBioMet
ms.assetid: 06BC3CBF-AB51-47C8-BCFB-ADC3D920F27B
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN, PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN callback, SensorAdapterSetCalibrationFormat, SensorAdapterSetCalibrationFormat callback function [Windows Biometric Framework API], secbiomet.sensoradaptersetcalibrationformat, winbio_adapter/SensorAdapterSetCalibrationFormat
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
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - SensorAdapterSetCalibrationFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_SET_CALIBRATION_FORMAT_FN callback function


## -description


Called by the Windows Biometric Framework to notify the sensor adapter that a particular calibration data format has been selected by the engine adapter.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param Format [in]

Address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536480">WINBIO_UUID</a> identifying the calibration data format selected by the Engine Adapter. 


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
The Sensor Adapter doesn’t support dynamic calibration. This is only treated as an error if the <a href="https://msdn.microsoft.com/F8C97013-3BDA-445F-A2C2-60D08DD9C71A">SensorAdapterQueryCalibrationFormats</a> method has previously indicated that the adapter supports dynamic calibration.

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



The Sensor Adapter should store a copy of this UUID value for later use in interpreting the contents of any calibration buffers sent to its <a href="https://msdn.microsoft.com/EE3B7066-BE91-4F63-8E0A-70F5CAB46496">SensorAdapterAcceptCalibrationData</a> method.



