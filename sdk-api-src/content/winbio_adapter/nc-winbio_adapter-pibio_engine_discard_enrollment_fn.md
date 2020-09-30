---
UID: NC:winbio_adapter.PIBIO_ENGINE_DISCARD_ENROLLMENT_FN
title: PIBIO_ENGINE_DISCARD_ENROLLMENT_FN (winbio_adapter.h)
description: Deletes intermediate enrollment state information from the pipeline.
helpviewer_keywords: ["EngineAdapterDiscardEnrollment","EngineAdapterDiscardEnrollment callback function [Windows Biometric Framework API]","PIBIO_ENGINE_DISCARD_ENROLLMENT_FN","PIBIO_ENGINE_DISCARD_ENROLLMENT_FN callback","secbiomet.engineadapterdiscardenrollment","winbio_adapter/EngineAdapterDiscardEnrollment"]
old-location: secbiomet\engineadapterdiscardenrollment.htm
tech.root: SecBioMet
ms.assetid: 305540bc-e0c6-460a-a00b-c295b3d6db93
ms.date: 12/05/2018
ms.keywords: EngineAdapterDiscardEnrollment, EngineAdapterDiscardEnrollment callback function [Windows Biometric Framework API], PIBIO_ENGINE_DISCARD_ENROLLMENT_FN, PIBIO_ENGINE_DISCARD_ENROLLMENT_FN callback, secbiomet.engineadapterdiscardenrollment, winbio_adapter/EngineAdapterDiscardEnrollment
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
 - PIBIO_ENGINE_DISCARD_ENROLLMENT_FN
 - winbio_adapter/PIBIO_ENGINE_DISCARD_ENROLLMENT_FN
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
 - EngineAdapterDiscardEnrollment
---

# PIBIO_ENGINE_DISCARD_ENROLLMENT_FN callback function


## -description

Called by the Windows Biometric Framework to delete intermediate enrollment state information from the pipeline.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it must return the following <b>HRESULT</b> value to indicate the error.

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
</table>

## -remarks

Your implementation of this function should not save information in the biometric unit database.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterDiscardEnrollment
//
// Purpose:
//      Deletes intermediate enrollment state information from the pipeline.
//
// Parameters:
//      Pipeline  - Pointer to a WINBIO_PIPELINE structure associated 
//                  with the biometric unit performing the operation
// 
static HRESULT
WINAPI
EngineAdapterDiscardEnrollment(
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

    // Return if an enrollment is not in progress. This example assumes that 
    // an enrollment object is part of your engine context structure.
    if (context->Enrollment.InProgress != TRUE)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }


    // Call a custom function (_AdapterDestroyEnrollmentTemplate) to release
    // any objects attached to the enrollment object.
    _AdapterDestroyEnrollmentTemplate(
        context,
        &context->Enrollment
        );

    // If the _AdapterDestroyEnrollmentTemplate function does not reset the
    // InProgress data member, reset it here.
    context->Enrollment.InProgress = FALSE;

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>