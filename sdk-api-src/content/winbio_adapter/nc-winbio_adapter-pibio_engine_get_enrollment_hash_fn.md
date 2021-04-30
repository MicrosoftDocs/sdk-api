---
UID: NC:winbio_adapter.PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN
title: PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN (winbio_adapter.h)
description: Retrieves the hash of the completed enrollment template in the pipeline.
helpviewer_keywords: ["EngineAdapterGetEnrollmentHash","EngineAdapterGetEnrollmentHash callback function [Windows Biometric Framework API]","PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN","PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN callback","secbiomet.engineadaptergetenrollmenthash","winbio_adapter/EngineAdapterGetEnrollmentHash"]
old-location: secbiomet\engineadaptergetenrollmenthash.htm
tech.root: SecBioMet
ms.assetid: 3a6984a1-0391-4e26-ad92-c07dc066acdb
ms.date: 12/05/2018
ms.keywords: EngineAdapterGetEnrollmentHash, EngineAdapterGetEnrollmentHash callback function [Windows Biometric Framework API], PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN, PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN callback, secbiomet.engineadaptergetenrollmenthash, winbio_adapter/EngineAdapterGetEnrollmentHash
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
 - PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN
 - winbio_adapter/PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN
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
 - EngineAdapterGetEnrollmentHash
---

# PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN callback function


## -description

Called by the Windows Biometric Framework to retrieve the hash of the completed enrollment template in the pipeline.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param HashValue [out]

Address of variable that receives a pointer to a byte array that contains the hash of the template.

### -param HashSize [out]

A pointer to a variable that receives the size, in bytes, of the hash pointed to  by the <i>HashValue</i> parameter.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The engine adapter does not support template hash generation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The pipeline does not contain a completed enrollment template.

</td>
</tr>
</table>

## -remarks

The template hashed by this function must be the completed enrollment template that will be stored in the database when <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn">EngineAdapterCommitEnrollment</a> is called. You must not hash one of the intermediate captured samples.

The algorithm used to generate the template hash is that which was selected by the most recent call, on this pipeline, to <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn">EngineAdapterSetHashAlgorithm</a>.

The memory that contains the hash is owned and managed by the engine adapter after the <i>EngineAdapterGetEnrollmentHash</i> function returns successfully. The engine adapter must keep the buffer address valid until the Framework calls any of the following functions:

<ul>
<li>
<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn">EngineAdapterClearContext</a>
</li>
<li>
<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn">EngineAdapterCommitEnrollment</a>
</li>
<li>
<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn">EngineAdapterDiscardEnrollment</a>
</li>
</ul>
The engine adapter must also maintain a separate hash buffer for each pipeline.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
//////////////////////////////////////////////////////////////////////////////////////////
//
// EngineAdapterGetEnrollmentHash
//
// Purpose:
//      Retrieves the hash of the completed enrollment template in the pipeline.
//
// Parameters:
//      Pipeline        - Pointer to a WINBIO_PIPELINE structure associated 
//                        with the biometric unit performing the operation
//      HashValue       - Contains the hash of the template
//      HashSize        - Size, in bytes, of the hash pointed to by the 
//                        HashValue parameter
//
static HRESULT
WINAPI
EngineAdapterGetEnrollmentHash(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PUCHAR *HashValue,
    __out PSIZE_T HashSize
    )
{
    ////////////////////////////////////////////////////////////////////////////
    // Return E_NOTIMPL here if your adapter does not support template hashing.
    ////////////////////////////////////////////////////////////////////////////

    HRESULT hr = S_OK;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(HashValue) ||
        !ARGUMENT_PRESENT(HashSize))
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

    // Initialize the hash.
    *HashValue = NULL;
    *HashSize = 0;

    // If your engine adapter supports template hashing, call a custom function
    // (_AdapterGenerateHashForTemplate) to calculate the hash of the new
    // enrollment template. The hash value should be saved in the adapter
    // context.
    hr = _AdapterGenerateHashForTemplate(
                context,
                context->Enrollment.Template, 
                context->Enrollment.TemplateSize,
                context->HashBuffer,
                &context->HashSize
                );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Return the hash to the caller.
    *HashValue = context->HashBuffer;
    *HashSize = context->HashSize;

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>
