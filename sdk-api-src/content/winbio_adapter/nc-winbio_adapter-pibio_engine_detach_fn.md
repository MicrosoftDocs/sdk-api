---
UID: NC:winbio_adapter.PIBIO_ENGINE_DETACH_FN
title: PIBIO_ENGINE_DETACH_FN (winbio_adapter.h)
description: Releases adapter-specific resources attached to the pipeline.E
helpviewer_keywords: ["EngineAdapterDetach","EngineAdapterDetach callback function [Windows Biometric Framework API]","PIBIO_ENGINE_DETACH_FN","PIBIO_ENGINE_DETACH_FN callback","secbiomet.engineadapterdetach","winbio_adapter/EngineAdapterDetach"]
old-location: secbiomet\engineadapterdetach.htm
tech.root: SecBioMet
ms.assetid: a4bc8ef1-6005-4661-9bb1-20ea08d9a125
ms.date: 12/05/2018
ms.keywords: EngineAdapterDetach, EngineAdapterDetach callback function [Windows Biometric Framework API], PIBIO_ENGINE_DETACH_FN, PIBIO_ENGINE_DETACH_FN callback, secbiomet.engineadapterdetach, winbio_adapter/EngineAdapterDetach
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
 - PIBIO_ENGINE_DETACH_FN
 - winbio_adapter/PIBIO_ENGINE_DETACH_FN
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
 - EngineAdapterDetach
---

# PIBIO_ENGINE_DETACH_FN callback function


## -description

Called by the Windows Biometric Framework immediately before an engine adapter is removed from the processing pipeline of the biometric unit. The purpose of this function is to release adapter specific resources attached to the pipeline.

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
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>EngineContext</b> field of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To prevent memory leaks, your implementation of the <i>EngineAdapterDetach</i> function must release the private <b>WINBIO_ENGINE_CONTEXT</b> structure pointed to by the  <b>EngineContext</b> member of the pipeline along with any other resources attached to the engine context.

If the <b>EngineContext</b> field in the pipeline object is <b>NULL</b> when this function is called, the pipeline was not properly initialized and you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b> to notify the Windows Biometric Framework of the problem.

Before returning S_OK, the <i>EngineAdapterDetach</i> function must set the <b>EngineContext</b> field of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure to <b>NULL</b> and the <b>EngineHandle</b> field to <b>INVALID_HANDLE_VALUE</b>.

This function is called after the storage adapter has been removed from the pipeline. Therefore, this function must not call any functions referenced by the <a href="/windows/win32/api/winbio_adapter/ns-winbio_adapter-winbio_storage_interface">WINBIO_STORAGE_INTERFACE</a> structure pointed to by the <b>StorageInterface</b> member of the pipeline object.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterDetach
//
// Purpose:
//      Releases adapter specific resources attached to the pipeline.
//      
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit.
//
static HRESULT
WINAPI
EngineAdapterDetach(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    PWINBIO_ENGINE_CONTEXT context = NULL;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline and assign it to a local
    // variable.
    context = (PWINBIO_ENGINE_CONTEXT)Pipeline->EngineContext;
    if (context == NULL)
    {
        goto cleanup;
    }

    // Set the context on the pipeline to NULL.
    Pipeline->EngineContext = NULL;

    // If your adapter supports software-based template hashing and you
    // opened a Cryptography Next Generation (CNG) hash object handle
    // during initialization, implement the following custom function to 
    // release the CNG resources.
    _AdapterCleanupCrypto(context);

    // Implement one or more custom routines to release any structures 
    // that remain attached to the context block. These structures can 
    // include the most recent feature set, the current enrollment template, 
    // and other custom defined objects.
    if (context->FeatureSet != NULL)
    {
        _AdapterRelease(context->FeatureSet);
        context->FeatureSet = NULL;
        context->FeatureSetSize = 0;
    }

    if (context->Enrollment.Template != NULL)
    {
        _AdapterRelease(context->Enrollment.Template);
        context->Enrollment.Template = NULL;
        context->Enrollment.TemplateSize = 0;
        context->Enrollment.SampleCount = 0;
    }

    if (context->SomePointerField != NULL)
    {
        _AdapterRelease(context->SomePointerField);
        context->SomePointerField = NULL;
    }

    // Release the context block.
    _AdapterRelease(context);

cleanup:

    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn">EngineAdapterAttach</a>



<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn">SensorAdapterDetach</a>
