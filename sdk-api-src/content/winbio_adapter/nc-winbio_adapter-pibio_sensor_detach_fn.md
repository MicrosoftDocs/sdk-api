---
UID: NC:winbio_adapter.PIBIO_SENSOR_DETACH_FN
title: PIBIO_SENSOR_DETACH_FN
author: windows-sdk-content
description: Releases adapter specific resources attached to the pipeline.
old-location: secbiomet\sensoradapterdetach.htm
tech.root: SecBioMet
ms.assetid: 58124c44-4343-44c1-84a2-c03455d68199
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PIBIO_SENSOR_DETACH_FN, PIBIO_SENSOR_DETACH_FN callback, SensorAdapterDetach, SensorAdapterDetach callback function [Windows Biometric Framework API], secbiomet.sensoradapterdetach, winbio_adapter/SensorAdapterDetach
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
 - SensorAdapterDetach
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_SENSOR_DETACH_FN callback function


## -description


Called by the Windows Biometric Framework immediately before a sensor adapter is removed from the processing pipeline of the biometric unit. The purpose of this function is to release adapter specific resources attached to the pipeline.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


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
The <b>SensorContext</b> field of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To prevent memory leaks, your implementation of the <i>SensorAdapterDetach</i> function must release the private <b>WINBIO_SENSOR_CONTEXT</b> structure pointed to by the  <b>SensorContext</b> member of the pipeline along with any other resources attached to the sensor context.

If the <b>SensorContext</b> field in the pipeline object is <b>NULL</b> when this function is called, the pipeline was not properly initialized and you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b> to notify the Windows Biometric Framework of the problem.

Before returning S_OK, this function must set the <b>SensorContext</b> field of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure to <b>NULL</b>.

Because this function is called after the storage and engine adapters have been removed from the pipeline, your implementation of this function must not call any functions referenced by the <a href="https://msdn.microsoft.com/04429f64-ae41-4c26-a777-bdb7aa92b685">WINBIO_ENGINE_INTERFACE</a> or <a href="https://msdn.microsoft.com/1cc7ce07-66df-43d9-9db2-50558a0f5f47">WINBIO_STORAGE_INTERFACE</a> structures pointed to by the <b>EngineInterface</b> and <b>StorageInterface</b> members of the pipeline object.

Because the <b>SensorHandle</b> member of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure will contain  a valid handle even after  <i>SensorAdapterDetach</i> is called, you can use the handle to access the sensor device if necessary. This function should not close the sensor handle. The Windows biometric Framework will do so after <i>SensorAdapterDetach</i> returns.


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
    if (Pipeline-&gt;SensorContext == NULL)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Cancel any pending I/O to the device.
    SensorAdapterCancel(Pipeline);

    // Take ownership of the sensor context from the pipeline.
    sensorContext = (PWINBIO_SENSOR_CONTEXT)Pipeline-&gt;SensorContext;
    Pipeline-&gt;SensorContext = NULL;

    // Release any structures that remain attached to the context block. 
    // The following example assumes that your sensor adapter context 
    // contains pointers to a capture buffer and an attributes buffer.
    if (sensorContext-&gt;CaptureBuffer != NULL)
    {
        // Zero the capture buffer.
        SecureZeroMemory(
            sensorContext-&gt;CaptureBuffer,
            sensorContext-&gt;CaptureBufferSize);

        // Release the capture buffer.
        _AdapterRelease(sensorContext-&gt;CaptureBuffer);
        sensorContext-&gt;CaptureBuffer = NULL;
        sensorContext-&gt;CaptureBufferSize = 0;
    }

    if (sensorContext-&gt;AttributesBuffer != NULL)
    {
        // Zero the attributes buffer.
        SecureZeroMemory(
            sensorContext-&gt;AttributesBuffer,
            sensorContext-&gt;AttributesBufferSize);

        // Release the attributes buffer.
        _AdapterRelease(sensorContext-&gt;AttributesBuffer);
        sensorContext-&gt;AttributesBuffer = NULL;
        sensorContext-&gt;AttributesBufferSize = 0;
    }

    // Close the overlapped I/O event handle.
    CloseHandle(sensorContext-&gt;Overlapped.hEvent);

    // Release the context structure.
    _AdapterRelease(sensorContext);
    sensorContext = NULL;
   
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/91243128-0543-4df9-bde8-74ef5ae46914">SensorAdapterAttach</a>



<a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a>
 

 

