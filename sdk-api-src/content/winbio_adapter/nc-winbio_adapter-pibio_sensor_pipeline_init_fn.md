---
UID: NC:winbio_adapter.PIBIO_SENSOR_PIPELINE_INIT_FN
title: PIBIO_SENSOR_PIPELINE_INIT_FN (winbio_adapter.h)
description: Gives the Sensor Adapter the chance to perform any initialization that remains incomplete, and which requires help from the Engine or Storage adapter components.
helpviewer_keywords: ["PIBIO_SENSOR_PIPELINE_INIT_FN","PIBIO_SENSOR_PIPELINE_INIT_FN callback","SensorAdapterPipelineInit","SensorAdapterPipelineInit callback function [Windows Biometric Framework API]","secbiomet.sensoradapterpipelineinit","winbio_adapter/SensorAdapterPipelineInit"]
old-location: secbiomet\sensoradapterpipelineinit.htm
tech.root: SecBioMet
ms.assetid: 91667505-78D6-405E-9028-DF4F3037B455
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_PIPELINE_INIT_FN, PIBIO_SENSOR_PIPELINE_INIT_FN callback, SensorAdapterPipelineInit, SensorAdapterPipelineInit callback function [Windows Biometric Framework API], secbiomet.sensoradapterpipelineinit, winbio_adapter/SensorAdapterPipelineInit
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
 - PIBIO_SENSOR_PIPELINE_INIT_FN
 - winbio_adapter/PIBIO_SENSOR_PIPELINE_INIT_FN
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
 - SensorAdapterPipelineInit
---

# PIBIO_SENSOR_PIPELINE_INIT_FN callback function


## -description

Called by the Windows Biometric Framework to give the Sensor Adapter the chance to perform any initialization that remains incomplete, and which requires help from the Engine or Storage adapter components.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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
Any error code will cause the Biometric Service to log the error and abort the configuration of the biometric unit.

</td>
</tr>
</table>

## -remarks

The Sensor Adapter should return <b>S_OK</b> if it doesn’t need to perform any initialization at this point.

When this routine is called, the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a>, <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a>, <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn">EngineAdapterPipelineInit</a>, and <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn">StorageAdapterPipelineInit</a> routines have completed normally.

This method executes in the context of an arbitrary RPC server thread.