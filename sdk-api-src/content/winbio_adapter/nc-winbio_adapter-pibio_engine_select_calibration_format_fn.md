---
UID: NC:winbio_adapter.PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN
title: PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN (winbio_adapter.h)
description: Called by the Windows Biometric Framework to determine which of the Sensor Adapter’s calibration formats the Engine Adapter wants to use.
helpviewer_keywords: ["EngineAdapterSelectCalibrationFormat","EngineAdapterSelectCalibrationFormat callback function [Windows Biometric Framework API]","PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN","PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN callback","secbiomet.engineadapterselectcalibrationformat","winbio_adapter/EngineAdapterSelectCalibrationFormat"]
old-location: secbiomet\engineadapterselectcalibrationformat.htm
tech.root: SecBioMet
ms.assetid: 1B4920D9-3C8E-4206-A71B-619A14ADD10A
ms.date: 12/05/2018
ms.keywords: EngineAdapterSelectCalibrationFormat, EngineAdapterSelectCalibrationFormat callback function [Windows Biometric Framework API], PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN, PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN callback, secbiomet.engineadapterselectcalibrationformat, winbio_adapter/EngineAdapterSelectCalibrationFormat
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
 - PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN
 - winbio_adapter/PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN
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
 - EngineAdapterSelectCalibrationFormat
---

# PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN callback function


## -description

Called by the Windows Biometric Framework to determine which of the Sensor Adapter’s calibration formats the Engine Adapter wants to use.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param FormatArray [in]

Address of an array of <a href="/windows-hardware/drivers/ddi/content/winbio_ioctl/ns-winbio_ioctl-_winbio_capture_parameters">WINBIO_UUID</a> items identifying the calibration data formats supported by the Sensor Adapter. The Engine Adapter is expected to choose one of these formats for its calibration data.

### -param FormatCount [in]

Value indicating the number of UUIDs in the <i>FormatArray</i> parameter.

### -param SelectedFormat [out]

Address of a <a href="/windows-hardware/drivers/ddi/content/winbio_ioctl/ns-winbio_ioctl-_winbio_capture_parameters">WINBIO_UUID</a> item where the <b>EngineAdapterSelectCalibrationFormat</b> method will store the UUID of the selected calibration format. This must be one of the UUIDs in the <i>FormatArray</i> parameter.

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