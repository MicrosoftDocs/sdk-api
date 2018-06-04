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

# PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN callback function


## -description


Called by the Windows Biometric Framework to determine which of the Sensor Adapter’s calibration formats the Engine Adapter wants to use.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param FormatArray [in]

Address of an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff536480">WINBIO_UUID</a> items identifying the calibration data formats supported by the Sensor Adapter. The Engine Adapter is expected to choose one of these formats for its calibration data.


### -param FormatCount [in]

Value indicating the number of UUIDs in the <i>FormatArray</i> parameter.


### -param SelectedFormat [out]

Address of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff536480">WINBIO_UUID</a> item where the <b>EngineAdapterSelectCalibrationFormat</b> method will store the UUID of the selected calibration format. This must be one of the UUIDs in the <i>FormatArray</i> parameter.


### -param MaxBufferSize [out]

Address of a variable where the <b>EngineAdapterSelectCalibrationFormat</b> method will store the maximum size (in bytes) of any calibration data it plans to return to the Sensor Adapter. The maximum size of this buffer must be 4096 bytes or less.


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
The operation succeeded. The <i>SelectedFormat</i> and <i>MaxBufferSize</i> return values have both been set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL </b></dt>
</dl>
</td>
<td width="60%">
The Engine Adapter doesn’t require dynamic calibration. This is not an error condition. The Biometric Service will convert this value to <b>S_OK</b>, and the biometric unit will be configured not to use dynamic calibration.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_NO_SUPPORTED_CALIBRATION_FORMAT </b></dt>
</dl>
</td>
<td width="60%">
The Engine Adapter requires dynamic calibration, but doesn’t support any of the calibration formats specified in the <i>FormatArray</i> parameter. (The Engine Adapter should also return this error code if the <i>FormatCount</i> argument is zero.) This error code will cause the Biometric Service to log the error and abort the configuration of the biometric unit.

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



This method is called once during configuration of the biometric unit. After a calibration format has been selected, it cannot be changed.



