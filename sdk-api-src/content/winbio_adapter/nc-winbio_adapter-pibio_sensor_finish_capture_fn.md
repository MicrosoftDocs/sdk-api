---
UID: NC:winbio_adapter.PIBIO_SENSOR_FINISH_CAPTURE_FN
title: PIBIO_SENSOR_FINISH_CAPTURE_FN (winbio_adapter.h)
description: The PIBIO_SENSOR_FINISH_CAPTURE_FN callback (winbio_adapter.h) retrieves a value that indicates whether the sensor indicator is on or off.
helpviewer_keywords: ["PIBIO_SENSOR_FINISH_CAPTURE_FN","PIBIO_SENSOR_FINISH_CAPTURE_FN callback","SensorAdapterFinishCapture","SensorAdapterFinishCapture callback function [Windows Biometric Framework API]","secbiomet.sensoradapterfinishcapture","winbio_adapter/SensorAdapterFinishCapture"]
old-location: secbiomet\sensoradapterfinishcapture.htm
tech.root: SecBioMet
ms.assetid: f9ede590-5208-40ed-ac62-604a2d13a5a6
ms.date: 08/03/2022
ms.keywords: PIBIO_SENSOR_FINISH_CAPTURE_FN, PIBIO_SENSOR_FINISH_CAPTURE_FN callback, SensorAdapterFinishCapture, SensorAdapterFinishCapture callback function [Windows Biometric Framework API], secbiomet.sensoradapterfinishcapture, winbio_adapter/SensorAdapterFinishCapture
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
 - PIBIO_SENSOR_FINISH_CAPTURE_FN
 - winbio_adapter/PIBIO_SENSOR_FINISH_CAPTURE_FN
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
 - SensorAdapterFinishCapture
---

# PIBIO_SENSOR_FINISH_CAPTURE_FN callback function


## -description

Called by the Windows Biometric Framework to wait for the completion of a capture operation initiated by the  <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn">SensorAdapterStartCapture</a> function.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param RejectDetail [out]

Pointer to a <b>WINBIO_REJECT_DETAIL</b> value that receives additional information about the failure to capture a biometric sample. If the operation succeeded, this parameter is set to zero. The following values are defined for fingerprint samples:

<ul>
<li>WINBIO_FP_TOO_HIGH</li>
<li>WINBIO_FP_TOO_LOW</li>
<li>WINBIO_FP_TOO_LEFT</li>
<li>WINBIO_FP_TOO_RIGHT</li>
<li>WINBIO_FP_TOO_FAST</li>
<li>WINBIO_FP_TOO_SLOW</li>
<li>WINBIO_FP_POOR_QUALITY</li>
<li>WINBIO_FP_TOO_SKEWED</li>
<li>WINBIO_FP_TOO_SHORT</li>
<li>WINBIO_FP_MERGE_FAILURE</li>
</ul>

## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. The following values will be recognized by the Windows Biometric Framework.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_BAD_CAPTURE</b></dt>
</dl>
</td>
<td width="60%">
The sample could not be captured. If you return this error code, you must also specify a value in the <i>RejectDetail</i> parameter that indicates the nature of the problem.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_CAPTURE_CANCELED</b></dt>
</dl>
</td>
<td width="60%">
The sensor driver returned <b>ERROR_CANCELLED</b> or <b>ERROR_OPERATION_ABORTED</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DEVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
There was a device failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b> or the <b>SensorHandle</b> member is set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
</table>

## -remarks

The Windows Biometric Framework calls this function after it successfully calls <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn">SensorAdapterStartCapture</a> or it calls <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn">SensorAdapterCancel</a>. It does not call this function if the call to <i>SensorAdapterStartCapture</i> fails.

When your implementation of this function  returns, the data in the pipeline should be ready for subsequent calls to functions such as <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn">SensorAdapterPushDataToEngine</a> or <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn">SensorAdapterExportSensorData</a>.

This is a blocking function that should return only after the sensor I/O operation has succeeded, failed, or been canceled. Typically, you will make this function block by passing the <b>OVERLAPPED</b> structure in the sensor adapter context to the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function. The <b>hEvent</b> handle in the <b>OVERLAPPED</b> structure must be signaled when <i>SensorAdapterFinishCapture</i> returns. The <i>GetOverlappedResult</i> function sets this handle automatically when it detects the end of a sensor I/O operation. If your adapter uses some other mechanism to detect I/O completion, you must signal the event yourself.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterFinishCapture
//
// Purpose:
//      Waits for the completion of a capture operation initiated by the 
//      SensorAdapterStartCapture function.
//      
// Parameters:
//      Pipeline     -  Pointer to a WINBIO_PIPELINE structure associated with 
//                      the biometric unit.
//      RejectDetail -  Pointer to a WINBIO_REJECT_DETAIL value that receives 
//                      additional information about the failure to capture a 
//                      biometric sample.
//
static HRESULT
WINAPI
SensorAdapterFinishCapture(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    )
{
    HRESULT hr = S_OK;
    WINBIO_SENSOR_STATUS sensorStatus = WINBIO_SENSOR_FAILURE;
    WINBIO_CAPTURE_PARAMETERS captureParameters = {0};
    BOOL result = TRUE;
    DWORD bytesReturned = 0;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(RejectDetail))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_SENSOR_CONTEXT sensorContext = 
             (PWINBIO_SENSOR_CONTEXT)Pipeline->SensorContext;

    // Verify the state of the pipeline.
    if (sensorContext == NULL || 
        Pipeline->SensorHandle == INVALID_HANDLE_VALUE)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Initialize the RejectDetail argument.
    *RejectDetail = 0;

    // Wait for I/O completion. This sample assumes that the I/O operation was 
    // started using the code example shown in the SensorAdapterStartCapture
    // documentation.
    SetLastError(ERROR_SUCCESS);

    result = GetOverlappedResult(
                Pipeline->SensorHandle,
                &sensorContext->Overlapped,
                &bytesReturned,
                TRUE
                );
    if (!result)
    {
        // There was an I/O error.
        return _AdapterGetHresultFromWin32(GetLastError());
    }

    if (bytesReturned == sizeof (DWORD))
    {
        // The buffer is not large enough.  This can happen if a device needs a 
        // bigger buffer depending on the purpose. Allocate a larger buffer and 
        // force the caller to reissue their I/O request.
        DWORD allocationSize = sensorContext->CaptureBuffer->PayloadSize;

        // Allocate at least the minimum buffer size needed to retrieve the 
        // payload structure.
        if (allocationSize < sizeof(WINBIO_CAPTURE_DATA))
        {
            allocationSize = sizeof(WINBIO_CAPTURE_DATA);
        }

        // Free the old buffer and allocate a new one.
        _AdapterRelease(sensorContext->CaptureBuffer);
        sensorContext->CaptureBuffer = NULL;

        sensorContext->CaptureBuffer = 
            (PWINBIO_CAPTURE_DATA)_AdapterAlloc(allocationSize);
        if (sensorContext->CaptureBuffer == NULL)
        {
            sensorContext->CaptureBufferSize = 0;
            return E_OUTOFMEMORY;
        }
        sensorContext->CaptureBufferSize = allocationSize;
        return WINBIO_E_BAD_CAPTURE;
    }

    // Normalize the status value before sending it back to the biometric service.
    if (sensorContext->CaptureBuffer != NULL &&
        sensorContext->CaptureBufferSize >= sizeof (WINBIO_CAPTURE_DATA))
    {
        switch (sensorContext->CaptureBuffer->SensorStatus)
        {
            case WINBIO_SENSOR_ACCEPT:
                // The capture was acceptable.
                break;

            case WINBIO_SENSOR_REJECT:
                // The capture was not acceptable. Overwrite the WinBioHresult value
                // in case it has not been properly set.
                sensorContext->CaptureBuffer->WinBioHresult = WINBIO_E_BAD_CAPTURE;
                break;

            case WINBIO_SENSOR_BUSY:
                // The device is busy. Reset the WinBioHresult value in case it 
                // has not been properly set.
                sensorContext->CaptureBuffer->WinBioHresult = WINBIO_E_DEVICE_BUSY;
                break;

            case WINBIO_SENSOR_READY:
            case WINBIO_SENSOR_NOT_CALIBRATED:
            case WINBIO_SENSOR_FAILURE:
            default:
                // There has been a device failure. Reset the WinBioHresult value
                // in case it has not been properly set.
                sensorContext->CaptureBuffer->WinBioHresult = WINBIO_E_INVALID_DEVICE_STATE;
                break;
        }

        *RejectDetail = sensorContext->CaptureBuffer->RejectDetail;
        hr = sensorContext->CaptureBuffer->WinBioHresult;
    }
    else
    {
        // The buffer is not large enough or the buffer pointer is NULL.
        hr = WINBIO_E_INVALID_DEVICE_STATE;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn">SensorAdapterCancel</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn">SensorAdapterExportSensorData</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn">SensorAdapterPushDataToEngine</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn">SensorAdapterStartCapture</a>
