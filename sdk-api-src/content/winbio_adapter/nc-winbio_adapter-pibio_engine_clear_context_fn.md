---
UID: NC:winbio_adapter.PIBIO_ENGINE_CLEAR_CONTEXT_FN
title: PIBIO_ENGINE_CLEAR_CONTEXT_FN (winbio_adapter.h)
description: Prepares the processing pipeline of the biometric unit for a new operation.E
helpviewer_keywords: ["EngineAdapterClearContext","EngineAdapterClearContext callback function [Windows Biometric Framework API]","PIBIO_ENGINE_CLEAR_CONTEXT_FN","PIBIO_ENGINE_CLEAR_CONTEXT_FN callback","secbiomet.engineadapterclearcontext","winbio_adapter/EngineAdapterClearContext"]
old-location: secbiomet\engineadapterclearcontext.htm
tech.root: SecBioMet
ms.assetid: c4ed5971-e657-4583-aac2-6263801f7468
ms.date: 12/05/2018
ms.keywords: EngineAdapterClearContext, EngineAdapterClearContext callback function [Windows Biometric Framework API], PIBIO_ENGINE_CLEAR_CONTEXT_FN, PIBIO_ENGINE_CLEAR_CONTEXT_FN callback, secbiomet.engineadapterclearcontext, winbio_adapter/EngineAdapterClearContext
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
 - PIBIO_ENGINE_CLEAR_CONTEXT_FN
 - winbio_adapter/PIBIO_ENGINE_CLEAR_CONTEXT_FN
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
 - EngineAdapterClearContext
---

# PIBIO_ENGINE_CLEAR_CONTEXT_FN callback function


## -description

Called by the Windows Biometric Framework to prepare the processing pipeline of the biometric unit for a new operation. This function should flush temporary data from the engine context and place the engine adapter into a well-defined initial state.

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
The <i>Pipeline</i> argument cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This purpose of this function is to reset the context to the state it was in immediately after a call to the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a> function. The context is a reusable structure. The <b>EngineAdapterClearContext</b> function reinitializes the context but does not remove it from the pipeline.

Typical examples of the objects in the engine adapter context area that should be cleared include the following.
<table>
<tr>
<th>Object</th>
<th>Description</th>
</tr>
<tr>
<td>Feature set</td>
<td>Contains a description of a biometric sample</td>
</tr>
<tr>
<td>Enrollment</td>
<td>Tracks the current state of an enrollment transaction.</td>
</tr>
<tr>
<td>Template</td>
<td>Biometric template created by the feature set or the enrollment object.</td>
</tr>
<tr>
<td>Comparison</td>
<td>Contains the result of a comparison between the template and the feature set.</td>
</tr>
<tr>
<td>Index vector</td>
<td>Contains a set of index values associated with the template.</td>
</tr>
</table>
 




#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterClearContext
//
// Purpose:
//      Prepares the processing pipeline of the biometric unit for a 
//      new operation.
//
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit.
//
static HRESULT
WINAPI
EngineAdapterClearContext(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_ENGINE_CONTEXT context = 
           (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;

    if (context == NULL)
    {
        goto cleanup;
    }

    // Change the engine adapter state and discard any partially completed
    // operations. Depending on the adapter, this can involve changes to state 
    // variables or actions implemented in hardware. The following example
    // assumes that your engine adapter context contains a ULONG data member 
    // and pointers to a feature set and an enrollment object.

    context->SomeField = 0L;

    if (context->FeatureSet != NULL)
    {
        // Zero the feature set if it contains unencrypted biometric data.
        SecureZeroMemory(
            context->FeatureSet,
            context->FeatureSetSize);

        // Release the feature set.
        _AdapterRelease(context->FeatureSet);
        context->FeatureSet = NULL;
        context->FeatureSetSize = 0;
    }

    if (context->Enrollment.Template != NULL)
    {
        // Zero the template if it contains unencrypted biometric data.
        SecureZeroMemory(
            context->Enrollment.Template,
            context->Enrollment.TemplateSize);

        // Release the template.
        _AdapterRelease(context->Enrollment.Template);
        context->Enrollment.Template = NULL;
        context->Enrollment.TemplateSize = 0;

        // Release other data members attached to the enrollment object.
        context->Enrollment.SampleCount = 0;
        context->Enrollment.InProgress = FALSE;
    }

cleanup:

    return S_OK;
}
```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn">SensorAdapterClearContext</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn">StorageAdapterClearContext</a>
