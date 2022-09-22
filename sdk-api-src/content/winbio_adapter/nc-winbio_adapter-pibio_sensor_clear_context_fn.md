---
UID: NC:winbio_adapter.PIBIO_SENSOR_CLEAR_CONTEXT_FN
title: PIBIO_SENSOR_CLEAR_CONTEXT_FN (winbio_adapter.h)
description: PIBIO_SENSOR_CLEAR_CONTEXT_FN (winbio_adapter.h) prepares the processing pipeline of the biometric unit for a new operation.
helpviewer_keywords: ["PIBIO_SENSOR_CLEAR_CONTEXT_FN","PIBIO_SENSOR_CLEAR_CONTEXT_FN callback","SensorAdapterClearContext","SensorAdapterClearContext callback function [Windows Biometric Framework API]","secbiomet.sensoradapterclearcontext","winbio_adapter/SensorAdapterClearContext"]
old-location: secbiomet\sensoradapterclearcontext.htm
tech.root: SecBioMet
ms.assetid: a0743004-aa79-41d8-87c7-2a1b6f00a1f2
ms.date: 08/04/2022
ms.keywords: PIBIO_SENSOR_CLEAR_CONTEXT_FN, PIBIO_SENSOR_CLEAR_CONTEXT_FN callback, SensorAdapterClearContext, SensorAdapterClearContext callback function [Windows Biometric Framework API], secbiomet.sensoradapterclearcontext, winbio_adapter/SensorAdapterClearContext
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
 - PIBIO_SENSOR_CLEAR_CONTEXT_FN
 - winbio_adapter/PIBIO_SENSOR_CLEAR_CONTEXT_FN
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
 - SensorAdapterClearContext
---

# PIBIO_SENSOR_CLEAR_CONTEXT_FN callback function


## -description

Called by the Windows Biometric Framework to prepare the processing pipeline of the biometric unit for a new operation. This function should flush temporary data from the sensor context and place the sensor adapter into a well-defined initial state.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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
The <i>Pipeline</i> argument cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Your implementation of the <b>SensorAdapterClearContext</b> function should clear the sample buffer.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterClearContext
//
// Purpose:
//      Prepare the processing pipeline for a new operation. This function 
//      should flush temporary data from the sensor context and place the 
//      sensor adapter into a well-defined initial state.
//      
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit.
//
static HRESULT
WINAPI
SensorAdapterClearContext(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_SENSOR_CONTEXT sensorContext = 
        (PWINBIO_SENSOR_CONTEXT)Pipeline->SensorContext;

    // Validate the current state of the sensor.
    if (sensorContext == NULL)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Change the sensor adapter state and discard any partially completed
    // operations. Depending on the adapter, this can involve changes to state 
    // variables or actions implemented in hardware. The following example
    // assumes that your sensor adapter context contains a ULONG data member 
    // and pointers to a capture buffer and an attributes buffer.

    sensorContext->SomeField = 0L;

    if (sensorContext->CaptureBuffer != NULL)
    {
        // Zero the capture buffer.
        SecureZeroMemory(
            sensorContext->CaptureBuffer,
            sensorContext->CaptureBufferSize);

        // Release the capture buffer.
        _AdapterRelease(sensorContext->CaptureBuffer);
        sensorContext->CaptureBuffer = NULL;
        sensorContext->CaptureBufferSize = 0;
    }

    if (sensorContext->AttributesBuffer != NULL)
    {
        // Zero the attributes buffer.
        SecureZeroMemory(
            sensorContext->AttributesBuffer,
            sensorContext->AttributesBufferSize);

        // Release the attributes buffer.
        _AdapterRelease(sensorContext->AttributesBuffer);
        sensorContext->AttributesBuffer = NULL;
        sensorContext->AttributesBufferSize = 0;
    }

    // TODO: Perform any other work required to clear the sensor context.

    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn">EngineAdapterClearContext</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn">StorageAdapterClearContext</a>
