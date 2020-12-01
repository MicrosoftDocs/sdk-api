---
UID: NC:winbio_adapter.PIBIO_STORAGE_ATTACH_FN
title: PIBIO_STORAGE_ATTACH_FN (winbio_adapter.h)
description: Adds a storage adapter to the processing pipeline of the biometric unit.
helpviewer_keywords: ["PIBIO_STORAGE_ATTACH_FN","PIBIO_STORAGE_ATTACH_FN callback","StorageAdapterAttach","StorageAdapterAttach callback function [Windows Biometric Framework API]","secbiomet.storageadapterattach","winbio_adapter/StorageAdapterAttach"]
old-location: secbiomet\storageadapterattach.htm
tech.root: SecBioMet
ms.assetid: 6abded6b-12e0-4cc6-a011-0b18e8ea747b
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_ATTACH_FN, PIBIO_STORAGE_ATTACH_FN callback, StorageAdapterAttach, StorageAdapterAttach callback function [Windows Biometric Framework API], secbiomet.storageadapterattach, winbio_adapter/StorageAdapterAttach
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
 - PIBIO_STORAGE_ATTACH_FN
 - winbio_adapter/PIBIO_STORAGE_ATTACH_FN
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
 - StorageAdapterAttach
---

# PIBIO_STORAGE_ATTACH_FN callback function


## -description

Called by the Windows Biometric Framework when a storage adapter is added to the processing pipeline of the biometric unit. The purpose of this function is to  perform any initialization required for later biometric operations.

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
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure pointed to by the <i>Pipeline</i> argument is not <b>NULL</b> or the <b>StorageHandle</b> member is not set to <b>INVALID_HANDLE_VALUE</b>.

</td>
</tr>
</table>

## -remarks

When implementing this function, you must allocate and manage any resources required by the adapter and attach these to the biometric unit pipeline. To do this, allocate a private <b>WINIBIO_STORAGE_CONTEXT</b> structure on the  heap, initialize it, and set its address in the <b>StorageContext</b> member of the pipeline object.

If the <b>StorageContext</b> field is not <b>NULL</b> when this function is called, the pipeline was not properly reset by a previous call to <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn">StorageAdapterDetach</a> and you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b> to notify the Windows Biometric Framework of the problem.

Similarly, if the <b>StorageHandle</b> field does not contain <b>INVALID_HANDLE_VALUE</b> when this function is called, you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b>.

If there is an error during the creation and initialization of storage adapter resources used by this function, you must perform any required cleanup before returning.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
/////////////////////////////////////////////////////////////////////////////////////////
//
// StorageAdapterAttach
//
// Purpose:
//      Performs any initialization required for later biometric operations.
//
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit performing the operation.
//
static HRESULT
WINAPI
StorageAdapterAttach(
    __inout PWINBIO_PIPELINE Pipeline
    )
{
    HRESULT hr = S_OK;
    PWINBIO_STORAGE_CONTEXT newContext = NULL;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    if (Pipeline->StorageContext != NULL ||
        Pipeline->StorageHandle != INVALID_HANDLE_VALUE)
    { 
        // The pipeline state is not valid. This function should never
        // be called if the pipeline already contains a storage context
        // or a valid storage handle.
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Call a custom function (_AdapterAlloc) to allocate memory to hold the 
    // sensor adapter context.
    newContext = (PWINBIO_STORAGE_CONTEXT)_AdapterAlloc(sizeof(WINBIO_STORAGE_CONTEXT));
    if (newContext == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto cleanup;
    }

    // Call a custom function to initialize the result set to be used by the next 
    // query operation. Initialization typically requires that you clear the result set
    // of any previous query, mark the set as empty, and place the result set cursor
    // in a known state.
    // The result set is attached to the storage context so that it can persist from
    // one storage adapter call to the next.  
    hr = _ResultSetInitialize(&newContext->ResultSet);
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // TODO: Initialize any other required context fields (not shown).


    // If initialization completes successfully, attach the context to the 
    // processing pipeline of the biometric unit.
    Pipeline->StorageContext = newContext;
    newContext = NULL;

cleanup:

    if (FAILED(hr) && newContext != NULL)
    {
        _ResultSetCleanup(&newContext->ResultSet);
        _AdapterRelease( newContext );
        newContext = NULL;
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn">StorageAdapterDetach</a>