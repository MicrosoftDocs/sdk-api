---
UID: NC:winbio_adapter.PIBIO_SENSOR_PIPELINE_CLEANUP_FN
title: PIBIO_SENSOR_PIPELINE_CLEANUP_FN (winbio_adapter.h)
description: Gives the Sensor Adapter the chance to perform any cleanup in that requires help from the Engine or Storage adapter components.helpviewer_keywords: ["PIBIO_SENSOR_PIPELINE_CLEANUP_FN","PIBIO_SENSOR_PIPELINE_CLEANUP_FN callback","SensorAdapterPipelineCleanup","SensorAdapterPipelineCleanup callback function [Windows Biometric Framework API]","secbiomet.sensoradapterpipelinecleanup","winbio_adapter/SensorAdapterPipelineCleanup"]
old-location: secbiomet\sensoradapterpipelinecleanup.htm
tech.root: SecBioMet
ms.assetid: 36238A6F-BDE2-454E-A183-ED10A455AF13
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_PIPELINE_CLEANUP_FN, PIBIO_SENSOR_PIPELINE_CLEANUP_FN callback, SensorAdapterPipelineCleanup, SensorAdapterPipelineCleanup callback function [Windows Biometric Framework API], secbiomet.sensoradapterpipelinecleanup, winbio_adapter/SensorAdapterPipelineCleanup
f1_keywords:
- winbio_adapter/SensorAdapterPipelineCleanup
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winbio_adapter.h
api_name:
- SensorAdapterPipelineCleanup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PIBIO_SENSOR_PIPELINE_CLEANUP_FN callback function


## -description


Called by the Windows Biometric Framework to give the Sensor Adapter the chance to perform any cleanup in that requires help from the Engine or Storage adapter components.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The Sensor Adapter should return <b>S_OK</b> if it doesn’t need to perform any cleanup at this point.

When this routine is called, the Engine and Storage adapters are still available.

This method executes in the context of an arbitrary RPC server thread.



