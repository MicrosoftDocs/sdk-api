---
UID: NC:winbio_adapter.PIBIO_SENSOR_ATTACH_FN
title: PIBIO_SENSOR_ATTACH_FN (winbio_adapter.h)
description: Adds a sensor adapter to the processing pipeline of the biometric unit.
helpviewer_keywords: ["PIBIO_SENSOR_ATTACH_FN","PIBIO_SENSOR_ATTACH_FN callback","SensorAdapterAttach","SensorAdapterAttach callback function [Windows Biometric Framework API]","secbiomet.sensoradapterattach","winbio_adapter/SensorAdapterAttach"]
old-location: secbiomet\sensoradapterattach.htm
tech.root: SecBioMet
ms.assetid: 91243128-0543-4df9-bde8-74ef5ae46914
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_ATTACH_FN, PIBIO_SENSOR_ATTACH_FN callback, SensorAdapterAttach, SensorAdapterAttach callback function [Windows Biometric Framework API], secbiomet.sensoradapterattach, winbio_adapter/SensorAdapterAttach
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
 - PIBIO_SENSOR_ATTACH_FN
 - winbio_adapter/PIBIO_SENSOR_ATTACH_FN
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
 - SensorAdapterAttach
---

# PIBIO_SENSOR_ATTACH_FN callback function


## -description

Called by the Windows Biometric Framework when a sensor adapter is added to the processing pipeline of the biometric unit. The purpose of this function is to  perform any initialization required for later biometric operations.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed because of insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is not <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This function is called before the engine and storage adapters have been initialized for the biometric unit. Therefore, this function must not call any functions referenced by the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_ENGINE_INTERFACE</a> or the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a> structure pointed to by the <b>EngineInterface</b> and <b>StorageInterface</b> members of the pipeline object.

Because the <b>SensorHandle</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure will contain  a valid handle before  this method is called, your implementation of <i>SensorAdapterAttach</i>  can use the handle to access the sensor device if necessary.

When implementing this function, you must allocate and manage any resources required by the adapter and attach these to the biometric unit pipeline. To do this, allocate a private <b>WINBIO_SENSOR_CONTEXT</b> structure on the  heap, initialize it, and set its address in the <b>SensorContext</b> member of the pipeline object.

If there is an error during the creation and initialization of engine adapter resources used by this function, you must perform any required cleanup before returning.

If the <b>SensorContext</b> field is not <b>NULL</b> when this function is called, the pipeline was not properly reset by a prior call to <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn">SensorAdapterDetach</a> and you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b> to notify the Windows Biometric Framework of the problem.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterAttach
//
// Purpose:
//      Performs any initialization required for later biometric operations.
//
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit performing the operation.
//
static HRESULT
WINAPI
SensorAdapterAttach(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    HRESULT hr = S_OK;
    PWINBIO_SENSOR_CONTEXT newContext = NULL;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Validate the current sensor state.
    if (Pipeline->SensorContext != NULL)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Use a custom function (_AdapterAlloc) to allocate memory for the 
    // sensor adapter context.
    newContext = (PWINBIO_SENSOR_CONTEXT)_AdapterAlloc(sizeof(WINBIO_SENSOR_CONTEXT));
    if (newContext == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto cleanup;
    }

    // Create a manual reset event to monitor overlapped I/O.
    newContext->Overlapped.hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (newContext->Overlapped.hEvent == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto cleanup;
    }

    // Initialize any required context fields. This example assumes that your
    // sensor context points to a capture buffer and an attributes buffer.
    newContext->CaptureBuffer = NULL;
    newContext->CaptureBufferSize = 0;

    newContext->AttributesBuffer = NULL;
    newContext->AttributesBufferSize = sizeof (WINBIO_SENSOR_ATTRIBUTES);

    // Transfer ownership of the new sensor context structure to the 
    // pipeline.
    Pipeline->SensorContext = newContext;
    newContext = NULL;

cleanup:

    if (FAILED(hr) && newContext != NULL)
    {
        CloseHandle( newContext->Overlapped.hEvent;
        _AdapterRelease( newContext );
        newContext = NULL;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn">SensorAdapterDetach</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a>



<a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a>