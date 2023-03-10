---
UID: NC:winbio_adapter.PIBIO_ENGINE_CREATE_ENROLLMENT_FN
title: PIBIO_ENGINE_CREATE_ENROLLMENT_FN (winbio_adapter.h)
description: Initializes the enrollment object in the biometric unit pipeline.
helpviewer_keywords: ["EngineAdapterCreateEnrollment","EngineAdapterCreateEnrollment callback function [Windows Biometric Framework API]","PIBIO_ENGINE_CREATE_ENROLLMENT_FN","PIBIO_ENGINE_CREATE_ENROLLMENT_FN callback","secbiomet.engineadaptercreateenrollment","winbio_adapter/EngineAdapterCreateEnrollment"]
old-location: secbiomet\engineadaptercreateenrollment.htm
tech.root: SecBioMet
ms.assetid: 5eec81ec-490c-485f-bbaf-4d972d7c8fde
ms.date: 12/05/2018
ms.keywords: EngineAdapterCreateEnrollment, EngineAdapterCreateEnrollment callback function [Windows Biometric Framework API], PIBIO_ENGINE_CREATE_ENROLLMENT_FN, PIBIO_ENGINE_CREATE_ENROLLMENT_FN callback, secbiomet.engineadaptercreateenrollment, winbio_adapter/EngineAdapterCreateEnrollment
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
 - PIBIO_ENGINE_CREATE_ENROLLMENT_FN
 - winbio_adapter/PIBIO_ENGINE_CREATE_ENROLLMENT_FN
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
 - EngineAdapterCreateEnrollment
---

# PIBIO_ENGINE_CREATE_ENROLLMENT_FN callback function


## -description

Called by the Windows Biometric Framework to initialize the enrollment object in the biometric unit pipeline.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete the operation.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn">EngineAdapterCommitEnrollment</a> marks the beginning of an enrollment transaction.  If this function succeeds, the Windows Biometric Framework calls <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn">EngineAdapterUpdateEnrollment</a> to add one or more feature sets to the enrollment object. The Framework then calls <i>EngineAdapterCommitEnrollment</i> or <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn">EngineAdapterDiscardEnrollment</a> to complete the transaction.



#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterCreateEnrollment
//
// Purpose:
//      Initialize the enrollment object in the biometric unit pipeline.
//
// Parameters:
//      Pipeline    - Pointer to a WINBIO_PIPELINE structure associated 
//                    with the biometric unit performing the operation
//
static HRESULT
WINAPI
EngineAdapterCreateEnrollment(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    HRESULT hr = S_OK;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT context = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    // Return if an enrollment is already in progress. This example assumes that 
    // your engine adapter context contains an enrollment object.
    if (context->Enrollment.InProgress == TRUE)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Call a custom function (_AdapterCreateEnrollmentTemplate) to create a 
    // new enrollment template and attach it to the engine adapter context.
    hr = _AdapterCreateEnrollmentTemplate( 
            context, 
            &context->Enrollment
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Initialize any Enrollment data members not initialized by  the 
    // _AdapterCreateEnrollmentTemplate function. This example assumes that
    // your enrollment object contains at a minimum a field that specifies 
    // the number of biometric samples and another that specifies whether a
    // new enrollment is in progress.
    context->Enrollment.SampleCount = 0;
    context->Enrollment.InProgress = TRUE;

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>