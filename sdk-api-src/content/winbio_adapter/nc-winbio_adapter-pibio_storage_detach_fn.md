---
UID: NC:winbio_adapter.PIBIO_STORAGE_DETACH_FN
title: PIBIO_STORAGE_DETACH_FN (winbio_adapter.h)
description: Releases adapter-specific resources attached to the pipeline.S
helpviewer_keywords: ["PIBIO_STORAGE_DETACH_FN","PIBIO_STORAGE_DETACH_FN callback","StorageAdapterDetach","StorageAdapterDetach callback function [Windows Biometric Framework API]","secbiomet.storageadapterdetach","winbio_adapter/StorageAdapterDetach"]
old-location: secbiomet\storageadapterdetach.htm
tech.root: SecBioMet
ms.assetid: cebf03d3-e393-437a-81f7-579fea95aa9c
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_DETACH_FN, PIBIO_STORAGE_DETACH_FN callback, StorageAdapterDetach, StorageAdapterDetach callback function [Windows Biometric Framework API], secbiomet.storageadapterdetach, winbio_adapter/StorageAdapterDetach
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
 - PIBIO_STORAGE_DETACH_FN
 - winbio_adapter/PIBIO_STORAGE_DETACH_FN
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
 - StorageAdapterDetach
---

# PIBIO_STORAGE_DETACH_FN callback function


## -description

Called by the Windows Biometric Framework immediately before a storage adapter is removed from the processing pipeline of the biometric unit. The purpose of this function is to release adapter specific resources attached to the pipeline.

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
The <b>StorageContext</b> field of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To prevent memory leaks, your implementation of the <i>StorageAdapterDetach</i> function must release the private <b>WINBIO_STORAGE_CONTEXT</b> structure pointed to by the  <b>StorageContext</b> member of the pipeline along with any other resources attached to the storage context.

If the <b>StorageContext</b> field in the pipeline object is <b>NULL</b> when this function is called, the pipeline was not properly initialized and you must return <b>WINBIO_E_INVALID_DEVICE_STATE</b> to notify the Windows Biometric Framework of the problem.

Before returning S_OK, this function must set the <b>StorageContext</b> field of the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure to <b>NULL</b> and the <b>StorageHandle</b> field to <b>INVALID_HANDLE_VALUE</b>.


#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
/////////////////////////////////////////////////////////////////////////////////////////
//
// StorageAdapterDetach
//
// Purpose:
//      Release adapter specific resources attached to the pipeline.
//
// Parameters:
//      Pipeline -  Pointer to a WINBIO_PIPELINE structure associated with 
//                  the biometric unit performing the operation.
//
static HRESULT
WINAPI
StorageAdapterDetach(
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
    PWINBIO_STORAGE_CONTEXT storageContext = 
           (PWINBIO_STORAGE_CONTEXT)Pipeline->StorageContext;

    // Verify the pipeline state.
    if (storageContext == NULL)
    {
        // The pipeline state is not valid. This function should never
        // be called if the storage context in the pipeline is already
        // closed.
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Release any structures attached to the context block.
    StorageAdapterClearContext(Pipeline);

    // Close the database.
    StorageAdapterCloseDatabase(Pipeline);

    // Remove the context from the pipeline.
    Pipeline->StorageContext = NULL;
    Pipeline->StorageHandle = INVALID_HANDLE_VALUE;

    // Clear the result set. Depending on your implementation, this action
    // can be performed by the StorageAdapterClearContext function called
    // earlier.
    ResultSetCleanup(&storageContext->ResultSet);

    // Release the adapter context.
    _AdapterRelease( storageContext );
    storageContext = NULL;

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn">StorageAdapterAttach</a>
