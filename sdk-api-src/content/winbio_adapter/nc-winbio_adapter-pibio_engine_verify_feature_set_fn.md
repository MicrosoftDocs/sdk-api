---
UID: NC:winbio_adapter.PIBIO_ENGINE_VERIFY_FEATURE_SET_FN
title: PIBIO_ENGINE_VERIFY_FEATURE_SET_FN (winbio_adapter.h)
description: Compares the template in the current feature set with a specific template in the database.
helpviewer_keywords: ["EngineAdapterVerifyFeatureSet","EngineAdapterVerifyFeatureSet callback function [Windows Biometric Framework API]","PIBIO_ENGINE_VERIFY_FEATURE_SET_FN","PIBIO_ENGINE_VERIFY_FEATURE_SET_FN callback","secbiomet.engineadapterverifyfeatureset","winbio_adapter/EngineAdapterVerifyFeatureSet"]
old-location: secbiomet\engineadapterverifyfeatureset.htm
tech.root: SecBioMet
ms.assetid: 64107d5b-3071-4bd4-9c2c-dd06006aec4d
ms.date: 12/05/2018
ms.keywords: EngineAdapterVerifyFeatureSet, EngineAdapterVerifyFeatureSet callback function [Windows Biometric Framework API], PIBIO_ENGINE_VERIFY_FEATURE_SET_FN, PIBIO_ENGINE_VERIFY_FEATURE_SET_FN callback, secbiomet.engineadapterverifyfeatureset, winbio_adapter/EngineAdapterVerifyFeatureSet
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
 - PIBIO_ENGINE_VERIFY_FEATURE_SET_FN
 - winbio_adapter/PIBIO_ENGINE_VERIFY_FEATURE_SET_FN
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
 - EngineAdapterVerifyFeatureSet
---

# PIBIO_ENGINE_VERIFY_FEATURE_SET_FN callback function


## -description

Called by the Windows Biometric Framework to compare the template in the current feature set with a specific template in the database. If the templates are equivalent, the engine adapter must set the Boolean value pointed to by the <i>Match</i> parameter to <b>TRUE</b>, return the matched template in the <i>PayloadBlob</i> parameter,  and return a hash of the template in the <i>HashValue</i> parameter.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param Identity [in]

Pointer to a  <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that contains a GUID or SID that is expected to match that of the template recovered from the database.

### -param SubFactor [in]

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that is expected to match that of the template recovered from the database.
See the Remarks section for more details.

### -param Match [out]

Pointer to a Boolean value that specifies whether the <i>Identity</i> and <i>SubFactor</i> parameters match those of the template recovered from the database. <b>TRUE</b> specifies that these values match.

### -param PayloadBlob [out]

Address of a variable that receives a pointer to the payload data saved with the template. If there is no payload data, set this value to <b>NULL</b>.

### -param PayloadBlobSize [out]

Pointer to a value that receives the size, in bytes, of the buffer specified in the <i>PayloadBlob</i> parameter. If there is no payload data stored with the template, set this value to zero.

### -param HashValue [out]

Address of a variable that receives a pointer to the hash of the template. If the engine adapter does not support hash generation, set this value to <b>NULL</b>.

### -param HashSize [out]

Pointer to a value that contains the size, in bytes, of the hash specified by the <i>HashValue</i> parameter. If the engine adapter does not support hash generation, set this value to zero.

### -param RejectDetail [out]

Pointer to a <b>WINBIO_REJECT_DETAIL</b> value that receives additional information if a capture failure prevents the engine from performing a matching operation. If the most-recent capture succeeded, set this parameter to zero. The following values are defined for fingerprint capture

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
A mandatory pointer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>SubFactor</i> parameter is not correct.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>   WINBIO_E_BAD_CAPTURE</b></dt>
</dl>
</td>
<td width="60%">
The feature set did not meet the internal requirements of the engine adapter for a verification operation. Further information about the failure is specified by the <i>RejectDetail</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
The feature set in the pipeline matches one stored in the database but it does not correspond to the combination of values passed in the <i>Identity</i> and <i>SubFactor</i> parameters.


</td>
</tr>
</table>

## -remarks

The <i>SubFactor</i> parameter specifies the sub-factor associated with the biometric template. The Windows Biometric Framework supports only fingerprint capture and can use the following constants to represent sub-type information.

<ul>
<li>WINBIO_ANSI_381_POS_RH_THUMB</li>
<li>WINBIO_ANSI_381_POS_RH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_RH_LITTLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_THUMB</li>
<li>WINBIO_ANSI_381_POS_LH_INDEX_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_MIDDLE_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_RING_FINGER</li>
<li>WINBIO_ANSI_381_POS_LH_LITTLE_FINGER</li>
<li>WINBIO_SUBTYPE_ANY</li>
</ul>
<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>SubFactor</i> parameter. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>
The algorithm used to generate the template hash is the one selected by the most recent call, on this pipeline, to the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn">EngineAdapterSetHashAlgorithm</a> function.

The hash value returned by this function, if any, is the hash of the enrollment template found in the database, not the matching template attached to the pipeline.

The <i>PayloadBlob</i> and <i>HashValue</i> buffers are owned and managed by the engine adapter after the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn">EngineAdapterIdentifyFeatureSet</a> function returns successfully. The engine adapter must keep the buffer address valid, for this pipeline, until the next call to <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn">EngineAdapterClearContext</a>.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterVerifyFeatureSet
//
// Purpose:
//      Compares the template in the current feature set with a specific 
//      template in the database.
//      
// Parameters:
//      Pipeline        - Pointer to a WINBIO_PIPELINE structure associated 
//                        with the biometric unit performing the operation
//      Identity        - GUID or SID that is expected to match that of the 
//                        template recovered from the database
//      SubFactor       - A WINBIO_BIOMETRIC_SUBTYPE value that is expected 
//                        to match that of the template recovered from the 
//                        database
//      Match           - A Boolean value that specifies whether the Identity 
//                        and SubFactor parameters match those of the template
//                        recovered from the database
//      PayloadBlob     - Payload data saved with the template
//      PayloadBlobSize - Size, in bytes, of the buffer specified in the 
//                        PayloadBlob parameter
//      HashValue       - Hash of the template
//      HashSize        - Size, in bytes, of the hash specified by the 
//                        HashValue parameter
//      RejectDetail    - Receives additional information if a capture failure 
//                        prevents the engine from performing a matching operation
// 
static HRESULT
WINAPI
EngineAdapterVerifyFeatureSet(
    __inout PWINBIO_PIPELINE Pipeline,
    __in PWINBIO_IDENTITY Identity,
    __in WINBIO_BIOMETRIC_SUBTYPE SubFactor,
    __out PBOOLEAN Match,
    __out PUCHAR *PayloadBlob,
    __out PSIZE_T PayloadBlobSize,
    __out PUCHAR *HashValue,
    __out PSIZE_T HashSize,
    __out PWINBIO_REJECT_DETAIL RejectDetail
    )
{
    HRESULT hr = S_OK;
    WINBIO_STORAGE_RECORD thisRecord;
    BOOLEAN match = FALSE;
    WINBIO_REJECT_DETAIL rejectDetail = 0;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(Identity) ||
        !ARGUMENT_PRESENT(Match) ||
        !ARGUMENT_PRESENT(PayloadBlob) ||
        !ARGUMENT_PRESENT(PayloadBlobSize) ||
        !ARGUMENT_PRESENT(HashValue) ||
        !ARGUMENT_PRESENT(HashSize) ||
        !ARGUMENT_PRESENT(RejectDetail))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT context = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    // Initialize the return values.
    *Match              = FALSE;
    *PayloadBlob        = NULL;
    *PayloadBlobSize    = 0;
    *HashValue          = NULL;
    *HashSize           = 0;
    *RejectDetail       = 0;

    // The biometric unit cannot perform verification or identification
    // operations while it is performing an enrollment sequence.
    if (context->Enrollment.InProgress == TRUE)
    {
        hr = WINBIO_E_ENROLLMENT_IN_PROGRESS;
        goto cleanup;
    }

    // Query the storage adapter to determine whether the Identity and 
    // SubFactor combination specified on input are in the database. If
    // they are not, there can be no match. WbioStorageQueryBySubject
    // is a wrapper function defined in the Winbio_adapter.h header file.
    hr = WbioStorageQueryBySubject( Pipeline, Identity, SubFactor);
    if (FAILED(hr))
    {
        if (hr == WINBIO_E_DATABASE_NO_RESULTS)
        {
            hr = WINBIO_E_NO_MATCH;
        }
        goto cleanup;
    }

    // Position the cursor on the first record in the database. 
    // WbioStorageFirstRecord is a wrapper function defined in the 
    // Winbio_adapter.h header file.
    hr = WbioStorageFirstRecord( Pipeline );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Retrieve the current template record for the Identity and SubFactor 
    // combination specified on input. 
    hr = WbioStorageGetCurrentRecord( Pipeline, &thisRecord );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Call a custom function (_AdapterCompareTemplateToCurrentFeatureSet)
    // to compare the feature set attached to the pipeline with the template 
    // retrieved from the database.
    // If the template and feature set do not match, return WINBIO_E_NO_MATCH
    // and set the Match parameter to FALSE.
    // If your custom function cannot process the feature set, return 
    // WINBIO_E_BAD_CAPTURE and set extended error information in the 
    // RejectDetail parameter.
    hr = _AdapterCompareTemplateToCurrentFeatureSet( 
                context, 
                context->FeatureSet,
                context->FeatureSetSize,
                thisRecord.TemplateBlob, 
                thisRecord.TemplateBlobSize,
                &match,
                RejectDetail 
                );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // If there is a match and if your engine adapter supports template
    // hashing, call a custom function (_AdapterGenerateHashForTemplate)
    // to calculate the hash. Save the hash value in the context area of
    // the engine adapter.
    // Skip this step if your adapter does not support template hashing.
    hr = _AdapterGenerateHashForTemplate(
                context,
                thisRecord.TemplateBlob, 
                thisRecord.TemplateBlobSize,
                context->HashBuffer,
                &context->HashSize
                );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Set the return values.
    *Match              = TRUE;
    *PayloadBlob        = thisRecord.PayloadBlob;
    *PayloadBlobSize    = thisRecord.PayloadBlobSize;
    *HashValue          = &context->HashBuffer;
    *HashSize           = context->HashSize;

cleanup:

    if (hr == WINBIO_E_DATABASE_NO_RESULTS)
    {
        hr = WINBIO_E_NO_MATCH;
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn">EngineAdapterIdentifyFeatureSet</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>
