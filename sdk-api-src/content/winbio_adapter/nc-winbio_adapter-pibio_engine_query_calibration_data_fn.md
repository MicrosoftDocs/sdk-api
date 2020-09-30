---
UID: NC:winbio_adapter.PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN
title: PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN (winbio_adapter.h)
description: Gets a set of post-capture calibration data from the engine adapter.
helpviewer_keywords: ["EngineAdapterQueryCalibrationData","EngineAdapterQueryCalibrationData callback function [Windows Biometric Framework API]","PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN","PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN callback","secbiomet.engineadapterquerycalibrationdata","winbio_adapter/EngineAdapterQueryCalibrationData"]
old-location: secbiomet\engineadapterquerycalibrationdata.htm
tech.root: SecBioMet
ms.assetid: 2BC0C6D4-931C-4CB8-9620-5F224F8F436F
ms.date: 12/05/2018
ms.keywords: EngineAdapterQueryCalibrationData, EngineAdapterQueryCalibrationData callback function [Windows Biometric Framework API], PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN, PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN callback, secbiomet.engineadapterquerycalibrationdata, winbio_adapter/EngineAdapterQueryCalibrationData
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
 - PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN
 - winbio_adapter/PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN
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
 - EngineAdapterQueryCalibrationData
---

# PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN callback function


## -description

Called by the Windows Biometric Framework to get a set of post-capture calibration data from the engine adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param DiscardAndRepeatCapture [out]

Address of a Boolean value that must be set by the <b>EngineAdapterQueryCalibrationData</b> method. This value indicates what the biometric service should do with the current sample after calibration is complete.

<ul>
<li>
<b>TRUE</b> indicates that the captured biometric sample is unusable. The biometric service will discard the sample and collect a new one.

</li>
<li>
<b>FALSE</b> indicates that the sample is usable and the Engine should be instructed to perform further operations on it.

</li>
</ul>

### -param CalibrationBuffer [out]

Address of an empty buffer where the method is expected to write its calibration data. The memory holding this buffer belongs to the biometric service, and the Engine Adapter must not keep any pointers to this buffer once the <b>EngineAdapterQueryCalibrationData</b> method returns.

### -param CalibrationBufferSize [out]

Address of a variable where the <b>EngineAdapterQueryCalibrationData</b> method will store the size (in bytes) of the calibration data it has written to <i>CalibrationBuffer</i>. This value must not exceed <i>MaxBufferSize</i>. 

If <b>EngineAdapterQueryCalibrationData</b> sets this value to zero, the contents of the <i>CalibrationBuffer</i> will be discarded without sending them to the Sensor Adapter. This is not an error condition; it simply indicates that the Engine Adapter doesn’t need to update the sensor’s calibration based on the current capture data.

### -param MaxBufferSize [in]

A value indicating the maximum space (in bytes) available to the Engine Adapter in the <i>CalibrationBuffer</i>.

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

The <b>EngineAdapterQueryCalibrationData</b> method can independently control the biometric service’s repeat-capture behavior and the calibration behavior by setting <i>DiscardAndRepeatCapture</i> and <i>CalibrationBufferSize</i>, respectively.

<table>
<tr>
<th>Desired Behavior</th>
<th><i>DiscardAndRepeatCapture</i></th>
<th><i>CalibrationBufferSize</i></th>
</tr>
<tr>
<td>Repeat capture after calibration.</td>
<td><b>TRUE</b></td>
<td>Non-zero</td>
</tr>
<tr>
<td>Repeat capture without calibration.</td>
<td><b>TRUE</b></td>
<td>Zero</td>
</tr>
<tr>
<td>Continue processing the sample after calibration.</td>
<td><b>FALSE</b></td>
<td>Non-zero</td>
</tr>
<tr>
<td>Continue processing the sample without calibration.</td>
<td><b>FALSE</b></td>
<td>Zero</td>
</tr>
</table>