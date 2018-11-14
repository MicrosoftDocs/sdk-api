---
UID: NC:winbio_adapter.PIBIO_STORAGE_DELETE_RECORD_FN
title: PIBIO_STORAGE_DELETE_RECORD_FN
author: windows-sdk-content
description: Deletes one or more templates from the database.
old-location: secbiomet\storageadapterdeleterecord.htm
tech.root: SecBioMet
ms.assetid: f1939410-1c1e-42e4-98d6-d8866d313ca1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PIBIO_STORAGE_DELETE_RECORD_FN, PIBIO_STORAGE_DELETE_RECORD_FN callback, StorageAdapterDeleteRecord, StorageAdapterDeleteRecord callback function [Windows Biometric Framework API], secbiomet.storageadapterdeleterecord, winbio_adapter/StorageAdapterDeleteRecord
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - StorageAdapterDeleteRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_STORAGE_DELETE_RECORD_FN callback function


## -description


Called by the Windows Biometric Framework to delete one or more templates from the database.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param Identity [in]

Pointer to a  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the GUID or SID of the template to delete.


### -param SubFactor [in]

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that specifies the sub-factor associated with the template to delete.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument specified by the <i>SubFactor</i> parameter is not valid or a member of the structure specified by the <i>Identity</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the record header.

</td>
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
<dt><b><b>WINBIO_E_DATABASE_CORRUPTED</b></b></dt>
</dl>
</td>
<td width="60%">
There is an unspecified problem with the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_NO_SUCH_RECORD</b></b></dt>
</dl>
</td>
<td width="60%">
No matching record could be found in the database.

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



If the <b>Type</b> field of the <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure pointed to by the <i>Identity</i> parameter is set to <b>WINBIO_IDENTITY_TYPE_WILDCARD</b> and the <i>SubFactor</i> parameter equals <b>WINBIO_SUBTYPE_ANY</b>, the storage adapter should delete all records from the database.

<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>SubFactor</i> parameter. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

</div>
<div> </div>

#### Examples

The following pseudocode shows one possible implementation of this function. The example does not compile. You must adapt it to suit your purpose.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>/////////////////////////////////////////////////////////////////////////////////////////
//
// StorageAdapterDeleteRecord
//
// Purpose:
//      Deletes one or more templates from the database.
//
// Parameters:
//      Pipeline  -  Pointer to a WINBIO_PIPELINE structure associated with 
//                   the biometric unit performing the operation.
//      Identity  -  Pointer to a WINBIO_IDENTITY structure that contains the GUID or 
//                   SID of the template to delete.
//      SubFactor -  A WINBIO_BIOMETRIC_SUBTYPE value that specifies the sub-factor 
//                   associated with the template to delete.
//
static HRESULT
WINAPI
StorageAdapterDeleteRecord(
    __inout PWINBIO_PIPELINE Pipeline,
    __in PWINBIO_IDENTITY Identity,
    __in WINBIO_BIOMETRIC_SUBTYPE SubFactor
    )
{
    HRESULT hr = S_OK;
    BOOL lockAcquired = FALSE;
    struct _MY_ADAPTER_FILE_HEADER fileHeader = {0};
    SIZE_T remainingRecords = 0;
    LARGE_INTEGER currentRecordOffset = {0};
    struct _MY_ADAPTER_RECORD_HEADER *recordHeader = NULL;
    SIZE_T recordHeaderSize = 0;
    struct _MY_ADAPTER_DPAPI_DATA protectedData = {0};
    SIZE_T deletedRecordCount = 0;

    // Check that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(Identity))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_STORAGE_CONTEXT storageContext = (PWINBIO_STORAGE_CONTEXT)Pipeline-&gt;StorageContext;

    // Verify the pipeline state.
    if (storageContext == NULL || storageContext-&gt;FileHandle == INVALID_HANDLE_VALUE)
    {
        hr =  WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Check the identity type.
    if (Identity-&gt;Type != WINBIO_ID_TYPE_GUID &amp;&amp;
        Identity-&gt;Type != WINBIO_ID_TYPE_SID &amp;&amp;
        Identity-&gt;Type != WINBIO_ID_TYPE_WILDCARD)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    if (Identity-&gt;Type == WINBIO_ID_TYPE_WILDCARD &amp;&amp;
        Identity-&gt;Value.Wildcard != WINBIO_IDENTITY_WILDCARD)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // Some kind of sub-factor information is mandatory, even if it's
    // just a wildcard.
    if (SubFactor == WINBIO_SUBTYPE_NO_INFORMATION)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // Lock the database for writing (EXCLUSIVE ownership).
    hr = _LockDatabase( Pipeline-&gt;StorageHandle, TRUE);
    if (FAILED(hr))
    {
        goto cleanup;
    }
    lockAcquired = TRUE;

    // Read the database header block into memory.
    hr = _ReadFileHeader( Pipeline-&gt;StorageHandle, &amp;fileHeader );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // For this operation, you need to update only the record header 
    // area, not the index vector area.
    recordHeaderSize = sizeof(struct _MY_ADAPTER_RECORD_HEADER);

    recordHeader = (struct _MY_ADAPTER_RECORD_HEADER*)_AdapterAlloc( recordHeaderSize );
    if (recordHeader == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto cleanup;
    }

    currentRecordOffset = _MY_ADAPTER_FIRST_RECORD_OFFSET;
    remainingRecords = fileHeader.TotalRecordCount;

    // Scan through all records looking for identity matches.
    while (remainingRecords &gt; 0)
    {
        SIZE_T recordSize = 0;
        BOOLEAN match = FALSE;

        hr = _ReadRecordHeader(
                Pipeline-&gt;StorageHandle,
                currentRecordOffset,
                recordHeader,
                recordHeaderSize
                );
        if (FAILED(hr))
        {
            goto cleanup;
        }

        recordSize = recordHeader-&gt;RecordSize;

        // Ignore records already marked for deletion.
        if ((recordHeader-&gt;Flags &amp; _MY_ADAPTER_FLAG_RECORD_DELETED) == 0)
        {
            hr = _MatchIdentity( 
                    Identity, 
                    SubFactor, 
                    &amp;recordHeader-&gt;Identity, 
                    recordHeader-&gt;SubFactor, 
                    &amp;match
                    );
            if (FAILED(hr))
            {
                goto cleanup;
            }

            if (match == TRUE)
            {
                // Mark the record as deleted and call a custom function 
                // (_WriteRecordHeader) to write the record header to disk. Space 
                // occupied by deleted records should be reclaimed when the last
                // thread that is using the database closes the file. Delaying 
                // reclamation until the last thread closes is necessary because 
                // there could be other threads whose result sets contain references 
                // to the deleted records.
                recordHeader-&gt;Flags |= _MY_ADAPTER_FLAG_RECORD_DELETED;
                hr = _WriteRecordHeader(
                        Pipeline-&gt;StorageHandle,
                        currentRecordOffset,
                        recordHeader,
                        recordHeaderSize
                        );
                if (FAILED(hr))
                {
                    goto cleanup;
                }
                ++fileHeader.DeletedRecordCount;
                ++deletedRecordCount;
            }
        }

        currentRecordOffset.QuadPart += recordSize;
        --remainingRecords;
    }

    // Write the updated file header to disk.
    hr = _WriteFileHeader( 
            Pipeline-&gt;StorageHandle, 
            &amp;fileHeader
            );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_CORRUPTED;
        goto cleanup;
    }

    //  Recompute the file hash and write it to the protected data area.
    hr = _ReadProtectedData(
            Pipeline-&gt;StorageHandle,
            &amp;protectedData
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    hr = _ComputeFileHash(
            Pipeline-&gt;StorageHandle,
            _MY_ADAPTER_DPAPI_BLOCK_OFFSET,
            (SIZE_T)(fileHeader.FirstFreeByte.QuadPart - 
                     _MY_ADAPTER_DPAPI_BLOCK_SIZE),
            protectedData.FileHash,
            _MY_ADAPTER_FILE_HASH_LENGTH,
            (PSIZE_T)&amp;protectedData.FileHashLength
            );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_CORRUPTED;
        goto cleanup;
    }

    hr = _WriteProtectedData(
                Pipeline-&gt;StorageHandle,
                &amp;protectedData
                );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_CORRUPTED;
        goto cleanup;
    }

cleanup:

    // Call the SecureZeroMemory function to overwrite the template encryption key 
    // on the stack.
    SecureZeroMemory( &amp;protectedData, sizeof(struct _MY_ADAPTER_DPAPI_DATA));

    if (recordHeader != NULL)
    {
        _AdapterRelease(recordHeader);
        recordHeader = NULL;
    }

    if (lockAcquired == TRUE)
    {
        _UnlockDatabase( Pipeline-&gt;StorageHandle);
        lockAcquired = FALSE;
    }

    if (SUCCEEDED(hr))
    {
        if (deletedRecordCount == 0)
        {
            hr = WINBIO_E_DATABASE_NO_SUCH_RECORD;
        }
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/889664e2-00e8-49b4-9754-4ca72dd44bbd">StorageAdapterAddRecord</a>
 

 

