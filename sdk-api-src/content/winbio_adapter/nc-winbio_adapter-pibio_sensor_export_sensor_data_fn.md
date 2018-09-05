---
UID: NC:winbio_adapter.PIBIO_SENSOR_EXPORT_SENSOR_DATA_FN
title: PIBIO_SENSOR_EXPORT_SENSOR_DATA_FN
author: windows-sdk-content
description: Retrieves the most recently captured biometric sample formatted as a standard WINBIO_BIR structure.
old-location: secbiomet\sensoradapterexportsensordata.htm
old-project: SecBioMet
ms.assetid: a6e45371-169b-42a8-9a53-dd7b2928a754
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PIBIO_SENSOR_EXPORT_SENSOR_DATA_FN, PIBIO_SENSOR_EXPORT_SENSOR_DATA_FN callback, SensorAdapterExportSensorData, SensorAdapterExportSensorData callback function [Windows Biometric Framework API], secbiomet.sensoradapterexportsensordata, winbio_adapter/SensorAdapterExportSensorData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.redist: 
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - SensorAdapterExportSensorData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_SENSOR_EXPORT_SENSOR_DATA_FN callback function


## -description


Called by the Windows Biometric Framework to retrieve a copy of the most recently captured biometric sample formatted as a standard <a href="https://msdn.microsoft.com/39cfab34-0416-4897-bf95-a1b3c3a6a7a1">WINBIO_BIR</a> structure.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.



### -param *SampleBuffer [out]

Address of a variable that receives a pointer to a <a href="https://msdn.microsoft.com/39cfab34-0416-4897-bf95-a1b3c3a6a7a1">WINBIO_BIR</a> structure that contains the sample.


### -param SampleSize [out]

Pointer to a variable that receives the size, in bytes, of the buffer specified by the <i>SampleBuffer</i> parameter.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to create the <a href="https://msdn.microsoft.com/39cfab34-0416-4897-bf95-a1b3c3a6a7a1">WINBIO_BIR</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_NO_CAPTURE_DATA </b></dt>
</dl>
</td>
<td width="60%">
No capture data exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not currently implemented.

</td>
</tr>
</table>
 




## -remarks



You must allocate the buffer to be returned in the <i>SampleBuffer</i> parameter from the process heap by using the <a href="https://msdn.microsoft.com/9a176312-0312-4cc1-baf5-949b346d983e">HeapAlloc</a> function. Once created, this  buffer becomes the property of the Windows Biometric Framework. Because the Framework deallocates this memory when finished using it, your implementation of this function  must not attempt to deallocate the buffer or save a pointer to it.  By not saving the pointer, you prevent other parts of the engine adapter from attempting to use the buffer after this function returns.


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
// SensorAdapterExportSensorData
//
// Purpose:
//      Retrieves a copy of the most recently captured biometric sample.
//      
// Parameters:
//      Pipeline     -  Pointer to a WINBIO_PIPELINE structure associated with 
//                      the biometric unit.
//      SampleBuffer -  Address of a variable that receives a pointer to a 
//                      WINBIO_BIR structure that contains the sample.
//      SampleSize   -  Pointer to a variable that receives the size, in bytes, 
//                      of the buffer specified by the SampleBuffer parameter.
//
static HRESULT
WINAPI
SensorAdapterExportSensorData(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PWINBIO_BIR *SampleBuffer,
    __out SIZE_T *SampleSize
    )
{
    PWINBIO_BIR sampleBuffer = NULL;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(SampleBuffer) ||
        !ARGUMENT_PRESENT(SampleSize))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_SENSOR_CONTEXT sensorContext = 
                 (PWINBIO_SENSOR_CONTEXT)Pipeline-&gt;SensorContext;

    // Verify the state of the pipeline.
    if (sensorContext == NULL)
    {
        return WINBIO_E_INVALID_DEVICE_STATE;
    }

    // Determine whether there is capture data to return.
    if (sensorContext-&gt;CaptureBuffer == NULL ||
        sensorContext-&gt;CaptureBuffer-&gt;CaptureData.Size == 0)
    {
        return WINBIO_E_NO_CAPTURE_DATA;
    }

    // Allocate a buffer, copy the data into it, and return
    // the buffer and buffer size to the caller.
    sampleBuffer = _AdapterAlloc(sensorContext-&gt;CaptureBuffer-&gt;CaptureData.Size);
    if (sampleBuffer == NULL)
    {
        return E_OUTOFMEMORY;
    }
    RtlCopyMemory(
        sampleBuffer, 
        sensorContext-&gt;CaptureBuffer-&gt;CaptureData.Data,
        sensorContext-&gt;CaptureBuffer-&gt;CaptureData.Size
        );

    *SampleBuffer = sampleBuffer;
    sampleBuffer = NULL;

    *SampleSize = Pipeline-&gt;SensorContext-&gt;CaptureBuffer-&gt;CaptureData.Size;  

    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

