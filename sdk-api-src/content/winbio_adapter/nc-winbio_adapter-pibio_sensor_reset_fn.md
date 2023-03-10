---
UID: NC:winbio_adapter.PIBIO_SENSOR_RESET_FN
title: PIBIO_SENSOR_RESET_FN (winbio_adapter.h)
description: Reinitializes the sensor.
helpviewer_keywords: ["PIBIO_SENSOR_RESET_FN","PIBIO_SENSOR_RESET_FN callback","SensorAdapterReset","SensorAdapterReset callback function [Windows Biometric Framework API]","secbiomet.sensoradapterreset","winbio_adapter/SensorAdapterReset"]
old-location: secbiomet\sensoradapterreset.htm
tech.root: SecBioMet
ms.assetid: 09a93726-2dff-4a8a-b36c-ad481a4f61b6
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_RESET_FN, PIBIO_SENSOR_RESET_FN callback, SensorAdapterReset, SensorAdapterReset callback function [Windows Biometric Framework API], secbiomet.sensoradapterreset, winbio_adapter/SensorAdapterReset
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_SENSOR_RESET_FN
 - winbio_adapter/PIBIO_SENSOR_RESET_FN
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
 - SensorAdapterReset
---

# PIBIO_SENSOR_RESET_FN callback function


## -description

Called by the Windows Biometric Framework to reinitialize the sensor. The specific details of the reset state are determined by the sensor hardware vendor.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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
A <i>Pipeline</i> argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DEVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
There was a hardware failure.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>