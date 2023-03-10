---
UID: NC:winbio_adapter.PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN
title: PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN (winbio_adapter.h)
description: Accepts a raw biometric sample and extracts a feature set.
helpviewer_keywords: ["EngineAdapterAcceptSampleData","EngineAdapterAcceptSampleData callback function [Windows Biometric Framework API]","PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN","PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN callback","secbiomet.engineadapteracceptsampledata","winbio_adapter/EngineAdapterAcceptSampleData"]
old-location: secbiomet\engineadapteracceptsampledata.htm
tech.root: SecBioMet
ms.assetid: fa6c5aa4-a9f4-421e-bc43-ced7fade4144
ms.date: 12/05/2018
ms.keywords: EngineAdapterAcceptSampleData, EngineAdapterAcceptSampleData callback function [Windows Biometric Framework API], PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN, PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN callback, secbiomet.engineadapteracceptsampledata, winbio_adapter/EngineAdapterAcceptSampleData
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
 - PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN
 - winbio_adapter/PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN
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
 - EngineAdapterAcceptSampleData
---

# PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN callback function


## -description

Called by the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn">SensorAdapterPushDataToEngine</a>  function implemented by the sensor adapter to notify the engine adapter to accept a raw biometric sample and extract a feature set. The feature set can be used for matching or enrollment.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param SampleBuffer [in]

Pointer to a <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure that contains the biometric sample to be processed.

### -param SampleSize [in]

A <b>SIZE_T</b> value that contains the size of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure returned in the <i>SampleBuffer</i> parameter.

### -param Purpose [in]

A <b>WINBIO_BIR_PURPOSE</b> bitmask that specifies the intended use of the sample.  The <b>WINBIO_BIR_PURPOSE</b> structure specifies the purpose for which capture data is to be used, and (as a result) how it should be optimized. This can be a bitwise <b>OR</b> of the following values:<ul>
<li>WINBIO_PURPOSE_VERIFY</li>
<li>WINBIO_PURPOSE_IDENTIFY</li>
<li>WINBIO_PURPOSE_ENROLL</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION</li>
<li>WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION</li>
</ul>

### -param RejectDetail [out]

A pointer to a <b>WINBIO_REJECT_DETAIL</b> value that receives additional information about the failure to process a biometric sample. If the operation succeeded, this parameter is set to zero. The following values are defined for fingerprint samples:

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>SampleSize</i> argument cannot be zero. The <i>Purpose</i> argument must be a  bitwise <b>OR</b> of the values listed in the parameter description.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Pipeline</i>, <i>SampleBuffer</i>,  and <i>RejectDetail</i> arguments cannot be <b>NULL</b>.

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
<dt><b>WINBIO_E_BAD_CAPTURE</b></dt>
</dl>
</td>
<td width="60%">
The data could not be processed to create the required feature set. The RejectDetail contains additional information about the failure.

</td>
</tr>
</table>

## -remarks

The feature set created by calling this function is retained in the biometric unit pipeline after the function returns. It replaces any previous feature set.

The sensor adapter implementation of the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn">SensorAdapterPushDataToEngine</a> function should use the following wrapper function (defined in Winbio_adapter.h) to call <i>EngineAdapterAcceptSampleData</i>:


```cpp
HRESULT WbioEngineAcceptSampleData(
__inout PWINBIO_PIPELINE Pipeline,
__in PWINBIO_BIR SampleBuffer,
__in SIZE_T SampleSize,
__in WINBIO_BIR_PURPOSE Purpose,
__out PWINBIO_REJECT_DETAIL RejectDetail
);
```


The <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure that is passed in  the <i>SampleBuffer</i> parameter  is the property of the sensor adapter. Because the sensor adapter controls the lifetime of the <b>WINBIO_BIR</b> object, the <i>EngineAdapterAcceptSampleData</i> function must not attempt to deallocate the structure or save a pointer to it.  By not saving the pointer, you prevent other parts of the engine adapter from attempting to use the <b>WINBIO_BIR</b> structure after the <i>EngineAdapterAcceptSampleData</i> function returns.

If the <b>Offset</b> field of the <b>StandardDataBlock</b> member of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure is greater than zero (indicating that the BIR contains a biometric sample in the standard data format), the <b>BiometricDataFormat</b> field of the <b>HeaderBlock</b> member must be set as follows:

<ul>
<li>The <b>Owner</b> field must be <b>WINBIO_ ANSI_381_FORMAT_OWNER</b>.</li>
<li>The <b>Type</b> field must be <b>WINBIO_ANSI_381_FORMAT_TYPE</b>.</li>
</ul>
This is the only standard data format supported by the Windows Biometric Framework.

The Windows Biometric Framework also assumes that the <b>HeaderBlock</b> member (a <a href="/windows/desktop/SecBioMet/winbio-bir-header">WINBIO_BIR_HEADER</a> structure) contains the <b>DataFlags</b> and <b>Purpose</b> values used by the sensor adapter to capture the sample.

Fingerprint sensors processing fingerprint samples and rejecting bad swipes in the Engine Adapter should also use valid values for <b>WINBIO_BIR_PURPOSE</b>.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterAcceptSampleData
//
// Purpose:
//      Notifies the engine adapter to accept a raw biometric sample and 
//      extract a feature set.
//
// Parameters:
//      Pipeline        - Pointer to a WINBIO_PIPELINE structure associated 
//                        with the biometric unit performing the operation. 
//      SampleBuffer    - Contains the biometric sample to be processed.
//      SampleSize      - Size of the structure returned in the SampleBuffer 
//                        parameter.
//      Purpose         - Specifies the intended use of the sample.
//      RejectDetail    - Receives additional information about the failure, 
//                        if any, to process a biometric sample.
//
static HRESULT
WINAPI
EngineAdapterAcceptSampleData(
    __inout PWINBIO_PIPELINE Pipeline,
    __in PWINBIO_BIR SampleBuffer,
    __in SIZE_T SampleSize,
    __in WINBIO_BIR_PURPOSE Purpose,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    )
{
    HRESULT hr = S_OK;
    PUCHAR featureSet = NULL;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline)     ||
        !ARGUMENT_PRESENT(SampleBuffer) ||
        !ARGUMENT_PRESENT(RejectDetail))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT context = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    // Verify that input arguments are valid.
    if (SampleSize == 0 ||
        Purpose == WINBIO_NO_PURPOSE_AVAILABLE)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // Release any feature set currently attached to the pipeline before
    // creating a new feature set.
    if (context->FeatureSet != NULL)
    {
        _AdapterRelease(context->FeatureSet);
        context->FeatureSet = NULL;
        context->FeatureSetSize = 0;
    }

    // An actual engine adapter would here process the contents of the sample 
    // buffer, generate a feature set suitable for the purpose(s) specified 
    // by the Purpose parameter, and attach the feature set to the pipeline. 
    // The following trivial example, however, creates a feature set simply
    // by making an exact copy of the raw sample.
    // If the sample data cannot be processed, return an HRESULT error code
    // of WINBIO_E_BAD_CAPTURE and set extended error information in the 
    // RejectDetail parameter.
    featureSet = (PUCHAR)_AdapterAlloc(SampleSize);
    if (featureSet == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto cleanup;
    }
    RtlCopyMemory(featureSet, SampleBuffer, SampleSize);
    context->FeatureSet = featureSet;
    featureSet = NULL;
    context->FeatureSetSize = SampleSize;

cleanup:

    if (FAILED(hr))
    {
        if (featureSet != NULL)
        {
            _AdapterRelease(featureSet);
        }
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn">EngineAdapterExportEngineData</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>