---
UID: NC:winbio_adapter.PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN
title: PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN (winbio_adapter.h)
description: Makes the current contents of the sample buffer available to the engine adapter.
helpviewer_keywords: ["PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN","PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN callback","SensorAdapterPushDataToEngine","SensorAdapterPushDataToEngine callback function [Windows Biometric Framework API]","WINBIO_DATA_FLAG_INTEGRITY","WINBIO_DATA_FLAG_PRIVACY","WINBIO_DATA_FLAG_RAW","WINBIO_DATA_FLAG_SIGNED","secbiomet.sensoradapterpushdatatoengine","winbio_adapter/SensorAdapterPushDataToEngine"]
old-location: secbiomet\sensoradapterpushdatatoengine.htm
tech.root: SecBioMet
ms.assetid: dea49f4b-668d-4b30-a16f-b74f260785c2
ms.date: 11/19/2020
ms.keywords: PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN, PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN callback, SensorAdapterPushDataToEngine, SensorAdapterPushDataToEngine callback function [Windows Biometric Framework API], WINBIO_DATA_FLAG_INTEGRITY, WINBIO_DATA_FLAG_PRIVACY, WINBIO_DATA_FLAG_RAW, WINBIO_DATA_FLAG_SIGNED, secbiomet.sensoradapterpushdatatoengine, winbio_adapter/SensorAdapterPushDataToEngine
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
 - PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN
 - winbio_adapter/PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN
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
 - SensorAdapterPushDataToEngine
---

# PIBIO_SENSOR_PUSH_DATA_TO_ENGINE_FN callback function


## -description

Called by the Windows Biometric Framework to make the current contents of the sample buffer available to the engine adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Purpose [in]

A value that specifies the properties of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure that will be passed to the engine. This can be a bitwise <b>OR</b> of the following security and processing level flags:


<ul>
<li>WINBIO_PURPOSE_VERIFY</li>
<li>WINBIO_PURPOSE_IDENTIFY</li>
<li>WINBIO_PURPOSE_ENROLL</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION</li>
</ul>

### -param Flags [in]

A value that specifies the format of the sample. This can be a bitwise <b>OR</b> of the following security and processing level flags:


* **WINBIO_DATA_FLAG_PRIVACY**

The sample should be encrypted.
            
            
* **WINBIO_DATA_FLAG_INTEGRITY**

The sample should be digitally signed or protected by a message authentication code (MAC).
            
            
* **WINBIO_DATA_FLAG_SIGNED**

If this flag and the <mark>WINBIO_DATA_FLAG_INTEGRITY</mark> flag are set, the sample should be signed. If this flag is not set but the <mark>WINBIO_DATA_FLAG_INTEGRITY</mark> flag is set, a MAC should be computed.
            
            
* **WINBIO_DATA_FLAG_RAW**

The sample should be placed in the <xref targtype="struct" rid="secbiomet.winbio_bir">WINBIO_BIR</xref> object in the format in which it was captured.


### -param RejectDetail [out]

A pointer to a <b>WINBIO_REJECT_DETAIL</b> value that contains  information about the previous failure to capture a biometric sample and therefore the reason that the sample buffer is empty. If an earlier capture succeeded, this parameter is set to zero. The following values are defined for fingerprint capture:

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
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_BAD_CAPTURE</b></dt>
</dl>
</td>
<td width="60%">
The sample data is not suitable for use. If you return this error code, you must also specify a value in the <i>RejectDetail</i> parameter to indicate the nature of the problem.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>SensorContext</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is <b>NULL</b>.

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
</table>

## -remarks

Your implementation of this function should convert raw data contained in the  sample buffer into a standard <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure and push this structure to the engine  by using the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn">EngineAdapterAcceptSampleData</a> function. The correct way to do this is to call the <b>WbioEngineAcceptSampleData</b> helper function defined in Winbio_adapter.h header file.


If the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn">EngineAdapterAcceptSampleData</a> function returns WINBIO_E_BAD_CAPTURE, your implementation of <i>SensorAdapterPushDataToEngine</i> should return the <i>RejectDetail</i> value propagated by the engine adapter. 


The sensor adapter retains ownership of the sample buffer passed to <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn">EngineAdapterAcceptSampleData</a>. The sensor adapter is responsible for releasing this buffer at some point after <i>EngineAdapterAcceptSampleData</i> returns.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// SensorAdapterPushDataToEngine
//
// Purpose:
//      Makes the current contents of the sample buffer available to the 
//      engine adapter.
//      
// Parameters:
//      Pipeline     -  Pointer to a WINBIO_PIPELINE structure associated with 
//                      the biometric unit.
//      Purpose      -  Specifies the properties of the WINBIO_BIR structure 
//                      that will be passed to the engine.
//      Flags        -  A value that specifies the format of the sample.
//      RejectDetail -  Pointer to a WINBIO_REJECT_DETAIL value that receives 
//                      additional information about the reason the sample
//                      buffer is empty.
//
static HRESULT
WINAPI
SensorAdapterPushDataToEngine(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIR_PURPOSE Purpose,
    __in WINBIO_BIR_DATA_FLAGS Flags,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    )
{
    HRESULT hr = S_OK;

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
    if (sensorContext == NULL)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    if (sensorContext->CaptureBuffer != NULL &&
        sensorContext->CaptureBufferSize >= sizeof (WINBIO_CAPTURE_DATA) &&
        sensorContext->CaptureBuffer->CaptureData.Size != 0 &&
        sensorContext->CaptureBuffer->SensorStatus == WINBIO_SENSOR_ACCEPT)
    {
        // There is valid capture data in the Pipeline. Call the 
        // WbioEngineAcceptSampleData function to notify the engine adapter, but
        // retain ownership of the buffer in the sensor adapter. 
        // WbioEngineAcceptSampleData is a wrapper function declared in the
        // Winbio_adapter.h header file.
        hr = WbioEngineAcceptSampleData(
                    Pipeline,
                    (PWINBIO_BIR)sensorContext->CaptureBuffer->CaptureData.Data,
                    sensorContext->CaptureBuffer->CaptureData.Size,
                    Purpose,
                    RejectDetail
                    );
    }
    else if (sensorContext->CaptureBuffer != NULL &&
             sensorContext->CaptureBufferSize >= sizeof (WINBIO_CAPTURE_DATA) &&
             sensorContext->CaptureBuffer->WinBioHresult == WINBIO_E_BAD_CAPTURE)
    {
        // The most recent capture was not acceptable.  Do not attempt to push 
        // the sample to the engine. Instead, simply return the reject detail
        // information generated by the previous capture.
        hr = sensorContext->CaptureBuffer->WinBioHresult;
        *RejectDetail = sensorContext->CaptureBuffer->RejectDetail;
    }
    else
    {
        hr = WINBIO_E_NO_CAPTURE_DATA;
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>