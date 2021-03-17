---
UID: NC:winbio_adapter.PIBIO_SENSOR_DETACH_FN
title: PIBIO_SENSOR_DETACH_FN (winbio_adapter.h)
description: Releases adapter specific resources attached to the pipeline.
helpviewer_keywords: ["PIBIO_SENSOR_DETACH_FN","PIBIO_SENSOR_DETACH_FN callback","SensorAdapterDetach","SensorAdapterDetach callback function [Windows Biometric Framework API]","secbiomet.sensoradapterdetach","winbio_adapter/SensorAdapterDetach"]
old-location: secbiomet\sensoradapterdetach.htm
tech.root: SecBioMet
ms.assetid: 58124c44-4343-44c1-84a2-c03455d68199
ms.date: 12/05/2018
ms.keywords: PIBIO_SENSOR_DETACH_FN, PIBIO_SENSOR_DETACH_FN callback, SensorAdapterDetach, SensorAdapterDetach callback function [Windows Biometric Framework API], secbiomet.sensoradapterdetach, winbio_adapter/SensorAdapterDetach
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
 - PIBIO_SENSOR_DETACH_FN
 - winbio_adapter/PIBIO_SENSOR_DETACH_FN
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
 - SensorAdapterDetach
---

# PIBIO_SENSOR_DETACH_FN callback function


## -description

Called by the Windows Biometric Framework immediately before a sensor adapter is removed from the processing pipeline of the biometric unit. The purpose of this function is to release adapter specific resources attached to the pipeline.

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
The <i>Pipeline</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> field of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To prevent memory leaks, your implementation of the <i>SensorAdapterDetach</i> function must release the private <b>WINBIO_SENSOR_CONTEXT</b> structure pointed to by the  <b>SensorContext</b> member of the pipeline along with any other resources attached to the sensor context.

If the <b>SensorContext</b> field in the pipeline object is <b>NULL</b> when this function is called, the pipeline was not properly initialized and you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b> to notify the Windows Biometric Framework of the problem.

Before returning S_OK, this function must set the <b>SensorContext</b> field of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure to <b>NULL</b>.

Because this function is called after the storage and engine adapters have been removed from the pipeline, your implementation of this function must not call any functions referenced by the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_ENGINE_INTERFACE</a> or <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a> structures pointed to by the <b>EngineInterface</b> and <b>StorageInterface</b> members of the pipeline object.

Because the <b>SensorHandle</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure will contain  a valid handle even after  <i>SensorAdapterDetach</i> is called, you can use the handle to access the sensor device if necessary. This function should not close the sensor handle. The Windows biometric Framework will do so after <i>SensorAdapterDetach</i> returns.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterDetach
//
// Purpose:
//      Cancels all pending sensor operations.
//      
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit.
//
static HRESULT
WINAPI
SensorAdapterDetach(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    PWINBIO_SENSOR_CONTEXT sensorContext = NULL;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }
 
    // Validate the current state of the sensor.
    if (Pipeline->SensorContext == NULL)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Cancel any pending I/O to the device.
    SensorAdapterCancel(Pipeline);

    // Take ownership of the sensor context from the pipeline.
    sensorContext = (PWINBIO_SENSOR_CONTEXT)Pipeline->SensorContext;
    Pipeline->SensorContext = NULL;

    // Release any structures that remain attached to the context block. 
    // The following example assumes that your sensor adapter context 
    // contains pointers to a capture buffer and an attributes buffer.
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

    // Close the overlapped I/O event handle.
    CloseHandle(sensorContext->Overlapped.hEvent);

    // Release the context structure.
    _AdapterRelease(sensorContext);
    sensorContext = NULL;
   
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn">SensorAdapterAttach</a>



<a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a>