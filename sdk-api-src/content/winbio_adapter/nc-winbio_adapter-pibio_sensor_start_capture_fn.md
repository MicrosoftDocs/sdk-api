---
UID: NC:winbio_adapter.PIBIO_SENSOR_START_CAPTURE_FN
title: PIBIO_SENSOR_START_CAPTURE_FN
author: windows-sdk-content
description: Begins an asynchronous biometric capture.
old-location: secbiomet\sensoradapterstartcapture.htm
old-project: SecBioMet
ms.assetid: 79922878-f5d3-4400-8c4f-2636323d7dcf
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: PIBIO_SENSOR_START_CAPTURE_FN, PIBIO_SENSOR_START_CAPTURE_FN callback, SensorAdapterStartCapture, SensorAdapterStartCapture callback function [Windows Biometric Framework API], secbiomet.sensoradapterstartcapture, winbio_adapter/SensorAdapterStartCapture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	SensorAdapterStartCapture
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_START_CAPTURE_FN callback function


## -description


Called by the Windows Biometric Framework to begin an asynchronous biometric capture.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param Purpose [in]

A <b>WINBIO_BIR_PURPOSE</b> bitmask that specifies the intended use of the sample.  This can be a bitwise <b>OR</b> of the following values:<ul>
<li>WINBIO_PURPOSE_VERIFY</li>
<li>WINBIO_PURPOSE_IDENTIFY</li>
<li>WINBIO_PURPOSE_ENROLL</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION</li>
</ul>


Some sensors have the ability to capture biometric information at multiple resolutions. If the <i>Purpose</i> parameter specifies more than one flag, your adapter should use the flag that represents the highest resolution to determine the resolution of the capture operation.



### -param *Overlapped [out]

Address of a variable that receives a pointer to an <b>OVERLAPPED</b> structure that tracks the state of the asynchronous capture operation. This structure is created and managed by the sensor adapter but is used by the Windows Biometric Framework for synchronization. For more information, see the Remarks section.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>Purpose</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DEVICE_BUSY </b></dt>
</dl>
</td>
<td width="60%">
The device is not ready to capture data.

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
The <b>SensorContext</b> member of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b> or the <b>SensorHandle</b> member is set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
</table>
 




## -remarks



This function does not block. If the adapter issues multiple commands to the sensor to prepare for a capture operation, all but the final command can be synchronous. The final command, issued immediately before <i>SensorAdapterStartCapture</i> returns control to the Windows Biometric Framework, must be asynchronous and must use overlapped I/O.

To use overlapped I/O, begin by adding an <b>OVERLAPPED</b> object to the definition of the private sensor adapter context structure. This structure is available to the adapter through the <b>SensorContext</b> field of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> object.

When you implement <a href="https://msdn.microsoft.com/91243128-0543-4df9-bde8-74ef5ae46914">SensorAdapterAttach</a>, you must perform the following actions to initialize the <b>OVERLAPPED</b> structure:

<ul>
<li>Clear the <b>OVERLAPPED</b> structure by calling the <a href="https://msdn.microsoft.com/b9d67559-c94f-4c94-bc36-0d03893df450">ZeroMemory</a> function.</li>
<li>Create a manual reset event object by using the <a href="https://msdn.microsoft.com/1f6d946e-c74c-4599-ac3d-b709216a0900">CreateEvent</a> function. It is critical that the event object be manual rather than  auto-reset. The use of auto-reset events in overlapped I/O can lead to an unrecoverable lack of response in the I/O processing operation.</li>
<li>Save the handle of this event in the <b>hEvent</b> member of the <b>OVERLAPPED</b> structure.</li>
</ul>
When you implement <a href="https://msdn.microsoft.com/58124c44-4343-44c1-84a2-c03455d68199">SensorAdapterDetach</a>, you must release the event object by calling the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function. It is important not to release this handle until after all input and output operations related to the capture have been completed or canceled.

The Windows Biometric Framework uses the <b>OVERLAPPED</b> object when it calls operating system functions such as <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> and <a href="https://msdn.microsoft.com/51afb13c-ea7a-407a-9f21-345d84f3b96b">WaitForMultipleObjects</a> to determine when the capture operation has completed.

The event handle in the <b>OVERLAPPED</b> structure must be in the non-signaled state when <i>SensorAdapterStartCapture</i> returns. Calling <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> to start an overlapped I/O operation automatically resets the event. If your adapter uses some other mechanism to start an I/O operation, you must reset the event yourself.

The Windows Biometric Framework guarantees that only one asynchronous I/O operation is outstanding at any time for each biometric unit. Consequently, the sensor adapter only needs one <b>OVERLAPPED</b> structure for each processing pipeline.

The Windows Biometric Framework opens and closes the sensor adapter handle and is responsible for ensuring that the handle has been configured for overlapped I/O.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterStartCapture
//
// Purpose:
//      Begins an asynchronous biometric capture.
//      
// Parameters:
//      Pipeline   -  Pointer to a WINBIO_PIPELINE structure associated with 
//                    the biometric unit.
//      Purpose    -  A WINBIO_BIR_PURPOSE bitmask that specifies the intended
//                    use of the sample.
//      Overlapped -  Receives a pointer to an OVERLAPPED structure.
//
static HRESULT 
WINAPI
SensorAdapterStartCapture(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_PURPOSE Purpose,
    __out LPOVERLAPPED *Overlapped
    )
{
    HRESULT hr = S_OK;
    WINBIO_SENSOR_STATUS sensorStatus = WINBIO_SENSOR_FAILURE;
    WINBIO_CAPTURE_PARAMETERS captureParameters = {0};
    BOOL result = TRUE;
    DWORD bytesReturned = 0;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(Purpose)  ||
        !ARGUMENT_PRESENT(Overlapped))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_SENSOR_CONTEXT sensorContext = 
                       (PWINBIO_SENSOR_CONTEXT)Pipeline-&gt;SensorContext;

    // Verify the state of the pipeline.
    if (sensorContext == NULL || 
        Pipeline-&gt;SensorHandle == INVALID_HANDLE_VALUE)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    *Overlapped = NULL;

    //  Synchronously retrieve the status.
    hr = SensorAdapterQueryStatus(Pipeline, &amp;sensorStatus);
    if (FAILED(hr))
    {
        return hr;
    }

    // Determine whether the sensor requires calibration.
    if (sensorStatus == WINBIO_SENSOR_NOT_CALIBRATED)
    {
        // Call a custom function that sends IOCTLs to
        // the sensor to calibrate it. This operation is
        // synchronous.
        hr = _SensorAdapterCalibrate(Pipeline);

        // Retrieve the status again to determine whether the 
        // sensor is ready.
        if (SUCCEEDED(hr))
        {
            hr = SensorAdapterQueryStatus(Pipeline, &amp;sensorStatus);
        }

        if (FAILED(hr))
        {
            return hr;
        }
    }
    if (sensorStatus == WINBIO_SENSOR_BUSY)
    {
        return WINBIO_E_DEVICE_BUSY;
    }

    if (sensorStatus != WINBIO_SENSOR_READY)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Determine whether the data format has been previously determined.
    // If it has not, find a format supported by both the engine and 
    // the sensor.
    if ((sensorContext-&gt;Format.Owner == 0) &amp;&amp;
        (sensorContext-&gt;Format.Type == 0))
    {

        // Retrieve the format preferred by the engine.
        hr = Pipeline-&gt;EngineInterface-&gt;QueryPreferredFormat(
                                            Pipeline,
                                            &amp;sensorContext-&gt;Format,
                                            &amp;sensorContext-&gt;VendorFormat
                                            );
        if (SUCCEEDED(hr))
        {
            // Call a private function that queries the sensor driver
            // and attaches an attribute array to the sensor context.
            // This operation is synchronous.
            hr = _SensorAdapterGetAttributes(Pipeline);
        }

        if (SUCCEEDED(hr))
        {
            // Search the sensor attributes array for the format
            // preferred by the engine adapter.
            DWORD i = 0;
            for (i = 0; i &lt; sensorContext-&gt;AttributesBuffer-&gt;SupportedFormatEntries; i++)
            {
                if ((sensorContext-&gt;AttributesBuffer-&gt;SupportedFormat[i].Owner == sensorContext-&gt;Format.Owner) &amp;&amp;
                    (sensorContext-&gt;AttributesBuffer-&gt;SupportedFormat[i].Type == sensorContext-&gt;Format.Type))
                {
                    break;
                }
            }

            if (i == sensorContext-&gt;AttributesBuffer-&gt;SupportedFormatEntries)
            {
                // No match was found. Use the default.
                sensorContext-&gt;Format.Owner = WINBIO_ANSI_381_FORMAT_OWNER;
                sensorContext-&gt;Format.Type = WINBIO_ANSI_381_FORMAT_TYPE;
            }
        }
        else
        {
            return hr;
        }
    }

    // Set up the parameter-input block needed for the IOCTL.
    captureParameters.PayloadSize = sizeof(WINBIO_CAPTURE_PARAMETERS);
    captureParameters.Purpose = Purpose;
    captureParameters.Format.Owner = sensorContext-&gt;Format.Owner;
    captureParameters.Format.Type = sensorContext-&gt;Format.Type;
    CopyMemory(&amp;captureParameters.VendorFormat, &amp;sensorContext-&gt;VendorFormat, sizeof (WINBIO_UUID));
    captureParameters.Flags = WINBIO_DATA_FLAG_RAW;

    // Determine whether a buffer has already been allocated for this sensor.
    if (sensorContext-&gt;CaptureBuffer == NULL)
    {
        DWORD allocationSize = 0;

        sensorContext-&gt;CaptureBufferSize = 0;

        // This sample assumes that the sensor driver returns
        // a fixed-size DWORD buffer containing the required
        // size of the capture buffer if it receives a buffer
        // that is smaller than sizeof(WINBIO_CAPTURE_DATA).
        //
        // Call the driver with a small buffer to get the 
        // allocation size required for this sensor.
        //
        // Because this operation is asynchronous, you must block 
        // and wait for it to complete.
        result = DeviceIoControl(
                    Pipeline-&gt;SensorHandle,
                    IOCTL_VENDOR_PRIVATE_CMD_CAPTURE_DATA,
                    &amp;captureParameters,
                    sizeof(WINBIO_CAPTURE_PARAMETERS),
                    &amp;allocationSize,
                    sizeof(DWORD),
                    &amp;bytesReturned,
                    &amp;sensorContext-&gt;Overlapped
                    );
        if (!result &amp;&amp; GetLastError() == ERROR_IO_PENDING)
        {
            SetLastError(ERROR_SUCCESS);

            result = GetOverlappedResult(
                        Pipeline-&gt;SensorHandle,
                        &amp;sensorContext-&gt;Overlapped,
                        &amp;bytesReturned,
                        TRUE
                        );
        }

        if (!result || bytesReturned != sizeof (DWORD))
        {
            // An error occurred.
            hr = _AdapterGetHresultFromWin32(GetLastError());
            return hr;
        }

        // Make sure that you allocate at least the minimum buffer 
        // size needed to get the payload structure.
        if (allocationSize &lt; sizeof(WINBIO_CAPTURE_DATA))
        {
            allocationSize = sizeof(WINBIO_CAPTURE_DATA);
        }

        // Allocate the buffer.
        sensorContext-&gt;CaptureBuffer = (PWINBIO_CAPTURE_DATA)_AdapterAlloc(allocationSize);
        if (!sensorContext-&gt;CaptureBuffer)
        {
            sensorContext-&gt;CaptureBufferSize = 0;
            return E_OUTOFMEMORY;
        }
        sensorContext-&gt;CaptureBufferSize = allocationSize;
    }
    else
    {
        // The buffer has already been allocated. Clear the buffer contents. 
        SensorAdapterClearContext(Pipeline);
    }

    // Send the capture request. Because this is an asynchronous operation,
    // the IOCTL call will return immediately regardless of 
    // whether the I/O has completed.
    result = DeviceIoControl(
                Pipeline-&gt;SensorHandle,
                IOCTL_VENDOR_PRIVATE_CMD_CAPTURE_DATA,
                &amp;captureParameters,
                sizeof (WINBIO_CAPTURE_PARAMETERS),
                sensorContext-&gt;CaptureBuffer,
                sensorContext-&gt;CaptureBufferSize,
                &amp;bytesReturned,
                &amp;sensorContext-&gt;Overlapped
                );

    if (result ||
        (!result &amp;&amp; GetLastError() == ERROR_IO_PENDING))
    {
        *Overlapped = &amp;sensorContext-&gt;Overlapped;
        return S_OK;
    }
    else
    {
        hr = _AdapterGetHresultFromWin32(GetLastError());
        return hr;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/f9ede590-5208-40ed-ac62-604a2d13a5a6">SensorAdapterFinishCapture</a>
 

 

