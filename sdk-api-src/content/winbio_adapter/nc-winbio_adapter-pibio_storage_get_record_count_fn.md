---
UID: NC:winbio_adapter.PIBIO_STORAGE_GET_RECORD_COUNT_FN
title: PIBIO_STORAGE_GET_RECORD_COUNT_FN (winbio_adapter.h)
description: Retrieves the number of template records in the pipeline result set.
helpviewer_keywords: ["PIBIO_STORAGE_GET_RECORD_COUNT_FN","PIBIO_STORAGE_GET_RECORD_COUNT_FN callback","StorageAdapterGetRecordCount","StorageAdapterGetRecordCount callback function [Windows Biometric Framework API]","secbiomet.storageadaptergetrecordcount","winbio_adapter/StorageAdapterGetRecordCount"]
old-location: secbiomet\storageadaptergetrecordcount.htm
tech.root: SecBioMet
ms.assetid: dc7891c3-33f7-498c-acb1-4687909debb7
ms.date: 12/05/2018
ms.keywords: PIBIO_STORAGE_GET_RECORD_COUNT_FN, PIBIO_STORAGE_GET_RECORD_COUNT_FN callback, StorageAdapterGetRecordCount, StorageAdapterGetRecordCount callback function [Windows Biometric Framework API], secbiomet.storageadaptergetrecordcount, winbio_adapter/StorageAdapterGetRecordCount
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
 - PIBIO_STORAGE_GET_RECORD_COUNT_FN
 - winbio_adapter/PIBIO_STORAGE_GET_RECORD_COUNT_FN
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
 - StorageAdapterGetRecordCount
---

# PIBIO_STORAGE_GET_RECORD_COUNT_FN callback function


## -description

Called by the Windows Biometric Framework or by the engine adapter to retrieve the number of template records in the pipeline result set.

## -parameters

### -param Pipeline [in, out]

Pointer to a <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param RecordCount [out]

Pointer to a variable that receives the number of template records in the result set.

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
A mandatory pointer argument is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DATABASE_NO_RESULTS</b></dt>
</dl>
</td>
<td width="60%">
The query was successful, but no matching records could be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b> or the <b>FileHandle</b> member is not valid.

</td>
</tr>
</table>

## -remarks

The number of records currently in the result set is determined by the most recent call to the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn">StorageAdapterQueryByContent</a> or the <a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn">StorageAdapterQueryBySubject</a> function.



#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.


```cpp
/////////////////////////////////////////////////////////////////////////////////////////
//
// StorageAdapterGetRecordCount
//
// Purpose:
//      Retrieves the number of template records in the pipeline result set.
//
// Parameters:
//      Pipeline    -  Pointer to a WINBIO_PIPELINE structure associated with 
//                     the biometric unit performing the operation.
//      RecordCount -  Pointer to a variable that receives the number of template 
//                     records in the result set.
//
static HRESULT
WINAPI
StorageAdapterGetRecordCount(
    __inout PWINBIO_PIPELINE Pipeline,
    __out PSIZE_T RecordCount
    )
{
    HRESULT hr = S_OK;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(RecordCount))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_STORAGE_CONTEXT storageContext = (PWINBIO_STORAGE_CONTEXT)Pipeline->StorageContext;

    // Verify the pipeline state.
    if (storageContext == NULL || storageContext->FileHandle == INVALID_HANDLE_VALUE)
    {
        hr =  WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Call a custom function (_ResultSetGetCount) to retrieve the number of
    // records that the most recent query left in the result set.
    hr = _ResultSetGetCount( &storageContext->ResultSet, RecordCount);

cleanup:

    return hr;
}

```

## -see-also

<a href="/windows/desktop/SecBioMet/plug-in-functions">Plug-in Functions</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn">StorageAdapterQueryByContent</a>



<a href="/windows/desktop/api/winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn">StorageAdapterQueryBySubject</a>