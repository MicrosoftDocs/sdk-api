---
UID: NC:winbio_adapter.PIBIO_ENGINE_PIPELINE_INIT_FN
title: PIBIO_ENGINE_PIPELINE_INIT_FN (winbio_adapter.h)
description: Gives the Engine Adapter the chance to perform any initialization that remains incomplete.
helpviewer_keywords: ["EngineAdapterPipelineInit","EngineAdapterPipelineInit callback function [Windows Biometric Framework API]","PIBIO_ENGINE_PIPELINE_INIT_FN","PIBIO_ENGINE_PIPELINE_INIT_FN callback","secbiomet.engineadapterpipelineinit","winbio_adapter/EngineAdapterPipelineInit"]
old-location: secbiomet\engineadapterpipelineinit.htm
tech.root: SecBioMet
ms.assetid: 69D4BB35-2E00-4FF6-8A69-DFCEFA5785A0
ms.date: 12/05/2018
ms.keywords: EngineAdapterPipelineInit, EngineAdapterPipelineInit callback function [Windows Biometric Framework API], PIBIO_ENGINE_PIPELINE_INIT_FN, PIBIO_ENGINE_PIPELINE_INIT_FN callback, secbiomet.engineadapterpipelineinit, winbio_adapter/EngineAdapterPipelineInit
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
 - PIBIO_ENGINE_PIPELINE_INIT_FN
 - winbio_adapter/PIBIO_ENGINE_PIPELINE_INIT_FN
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
 - EngineAdapterPipelineInit
---

# PIBIO_ENGINE_PIPELINE_INIT_FN callback function


## -description

Called by the Windows Biometric Framework to give the Engine Adapter the chance to perform any initialization that remains incomplete.

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

The Engine Adapter should return <b>S_OK</b> if it doesn’t need to perform any initialization at this point.

When this routine is called, the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn">SensorAdapterAttach</a>, <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a>, and,<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a> routines have completed normally, the template database is open, and the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn">StorageAdapterPipelineInit</a> routine has completed normally.

This method executes in the context of an arbitrary RPC server thread.