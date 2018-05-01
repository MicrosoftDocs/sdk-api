---
UID: NC:winbio_adapter.PIBIO_SENSOR_ACCEPT_CALIBRATION_DATA_FN
title: PIBIO_SENSOR_ACCEPT_CALIBRATION_DATA_FN
author: windows-driver-content
description: Passes calibration data from the engine adapter to the sensor adapter.
old-location: secbiomet\sensoradapteracceptcalibrationdata.htm
old-project: SecBioMet
ms.assetid: EE3B7066-BE91-4F63-8E0A-70F5CAB46496
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PIBIO_SENSOR_ACCEPT_CALIBRATION_DATA_FN, SensorAdapterAcceptCalibrationData, SensorAdapterAcceptCalibrationData callback function [Windows Biometric Framework API], secbiomet.sensoradapteracceptcalibrationdata, winbio_adapter/SensorAdapterAcceptCalibrationData
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	SensorAdapterAcceptCalibrationData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_ACCEPT_CALIBRATION_DATA_FN callback


## -description


Called by the Windows Biometric Framework to pass calibration data from the engine adapter to the sensor adapter.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param CalibrationBuffer [in]

Pointer to the buffer that contains the calibration data.


### -param CalibrationBufferSize [in]

The size in bytes of the calibration buffer.


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
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Any error code will cause the Biometric Service to discontinue the dynamic calibration loop and abort the capture operation.

</td>
</tr>
</table>
 




## -remarks



This method is called during a dynamic calibration loop.

The memory holding the calibration buffer belongs to the Windows Biometric Framework, and the Sensor Adapter must not keep any pointers to this buffer once the <b>SensorAdapterAcceptCalibrationData</b> method returns.



