---
UID: NC:winbio_adapter.PIBIO_ENGINE_CREATE_ENROLLMENT_FN
title: PIBIO_ENGINE_CREATE_ENROLLMENT_FN
author: windows-sdk-content
description: Initializes the enrollment object in the biometric unit pipeline.
old-location: secbiomet\engineadaptercreateenrollment.htm
tech.root: SecBioMet
ms.assetid: 5eec81ec-490c-485f-bbaf-4d972d7c8fde
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EngineAdapterCreateEnrollment, EngineAdapterCreateEnrollment callback function [Windows Biometric Framework API], PIBIO_ENGINE_CREATE_ENROLLMENT_FN, PIBIO_ENGINE_CREATE_ENROLLMENT_FN callback, secbiomet.engineadaptercreateenrollment, winbio_adapter/EngineAdapterCreateEnrollment
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
 - EngineAdapterCreateEnrollment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_ENGINE_CREATE_ENROLLMENT_FN callback function


## -description


Called by the Windows Biometric Framework to initialize the enrollment object in the biometric unit pipeline.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


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



The <a href="https://msdn.microsoft.com/f8eb3dd9-b993-4b45-b7f4-e1925c233a80">EngineAdapterCommitEnrollment</a> marks the beginning of an enrollment transaction.  If this function succeeds, the Windows Biometric Framework calls <a href="https://msdn.microsoft.com/cd41be8c-fa78-4746-a9ad-c8385ed84b52">EngineAdapterUpdateEnrollment</a> to add one or more feature sets to the enrollment object. The Framework then calls <i>EngineAdapterCommitEnrollment</i> or <a href="https://msdn.microsoft.com/305540bc-e0c6-460a-a00b-c295b3d6db93">EngineAdapterDiscardEnrollment</a> to complete the transaction.



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




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>
 

 

