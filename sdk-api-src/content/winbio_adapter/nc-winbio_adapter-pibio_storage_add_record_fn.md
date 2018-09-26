---
UID: NC:winbio_adapter.PIBIO_STORAGE_ADD_RECORD_FN
title: PIBIO_STORAGE_ADD_RECORD_FN
author: windows-sdk-content
description: Adds a template to the database.
old-location: secbiomet\storageadapteraddrecord.htm
tech.root: SecBioMet
ms.assetid: 889664e2-00e8-49b4-9754-4ca72dd44bbd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PIBIO_STORAGE_ADD_RECORD_FN, PIBIO_STORAGE_ADD_RECORD_FN callback, StorageAdapterAddRecord, StorageAdapterAddRecord callback function [Windows Biometric Framework API], secbiomet.storageadapteraddrecord, winbio_adapter/StorageAdapterAddRecord
ms.prod: windows
ms.technology: windows-sdk
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
 - StorageAdapterAddRecord
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_STORAGE_ADD_RECORD_FN callback function


## -description


Called by the engine adapter to add a template to the database.


## -parameters




### -param Pipeline [in, out]

Pointer to the <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param RecordContents [in]

Pointer to a <a href="https://msdn.microsoft.com/fd638a08-cff0-4984-8580-a1eecd509a1f">WINBIO_STORAGE_RECORD</a> structure that contains the template to add.


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
A member of the  structure specified by the <i>RecordContents</i> parameter  is not valid.

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
<dt><b><b>WINBIO_E_DATABASE_BAD_INDEX_VECTOR</b></b></dt>
</dl>
</td>
<td width="60%">
The size of the  index vector specified in the <a href="https://msdn.microsoft.com/fd638a08-cff0-4984-8580-a1eecd509a1f">WINBIO_STORAGE_RECORD</a> structure does not match the index size specified when the database was created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DUPLICATE_ENROLLMENT</b></b></dt>
</dl>
</td>
<td width="60%">
The database already contains a template with the combination of values specified by the <i>Identity</i> and <i>SubFactor</i> parameters.


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
<dt><b><b>WINBIO_E_DATABASE_FULL</b></b></dt>
</dl>
</td>
<td width="60%">
The database is full and no further records can be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_LOCKED</b></b></dt>
</dl>
</td>
<td width="60%">
The database is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_WRITE_ERROR</b></b></dt>
</dl>
</td>
<td width="60%">
Record addition failed because of an unspecified problem.

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



The memory identified by the <i>RecordContents</i> parameter is the property of the Windows Biometric Framework. The storage adapter must not keep a copy of this pointer, or of any pointers contained in the <a href="https://msdn.microsoft.com/fd638a08-cff0-4984-8580-a1eecd509a1f">WINBIO_STORAGE_RECORD</a> structure, after returning from <i>StorageAdapterAddRecord</i>.


<div class="alert"><b>Important</b>  <p class="note">Do not attempt to validate the value supplied for the <i>SubFactor</i> value of the <i>RecordContents</i> parameter. The Windows Biometrics Service will validate the supplied value before passing it through to your implementation. If the value is <b>WINBIO_SUBTYPE_NO_INFORMATION</b> or <b>WINBIO_SUBTYPE_ANY</b>, then validate where appropriate.

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
// StorageAdapterAddRecord
//
// Purpose:
//      Adds a template to the database.
//
// Parameters:
//      Pipeline       - Pointer to a WINBIO_PIPELINE structure associated with 
//                       the biometric unit performing the operation.
//      RecordContents - Pointer to a WINBIO_STORAGE_RECORD structure that contains 
//                       the template to add.
//
static HRESULT
WINAPI
StorageAdapterAddRecord(
    __inout PWINBIO_PIPELINE Pipeline,
    __in PWINBIO_STORAGE_RECORD RecordContents
    )
{
    HRESULT hr = S_OK;
    struct _MY_ADAPTER_RECORD_HEADER *newRecord = NULL;
    SIZE_T newRecordSize = 0;
    BOOL lockAcquired = FALSE;
    ULONG index = 0;
    PUCHAR encryptedTemplateBlob = NULL;
    SIZE_T encryptedTemplateBlobSize = 0;
    struct _MY_ADAPTER_FILE_HEADER fileHeader = {0};
    SIZE_T templateBlobOffset = 0;
    SIZE_T payloadBlobOffset = 0;
    struct _MY_ADAPTER_DPAPI_DATA protectedData = {0};
    SIZE_T duplicateRecordCount = 0;

    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(RecordContents))
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

    // Check various values associated with the record contents. The
    // following example code assumes that a database record contains
    // a valid:
    //    Identity
    //    Sub-factor characteristic
    //    Biometric template
    //    Payload associated with the template
    //    Index vector
    //
    if (!ARGUMENT_PRESENT(RecordContents-&gt;Identity))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    if (RecordContents-&gt;Identity-&gt;Type != WINBIO_ID_TYPE_GUID &amp;&amp;
        RecordContents-&gt;Identity-&gt;Type != WINBIO_ID_TYPE_SID)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    if (RecordContents-&gt;SubFactor == WINBIO_SUBTYPE_NO_INFORMATION ||
        RecordContents-&gt;SubFactor == WINBIO_SUBTYPE_ANY)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    if (RecordContents-&gt;TemplateBlobSize == 0 ||
        !ARGUMENT_PRESENT(RecordContents-&gt;TemplateBlob))
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    if (RecordContents-&gt;PayloadBlobSize &gt; 0 &amp;&amp; 
        !ARGUMENT_PRESENT(RecordContents-&gt;PayloadBlob))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    if (RecordContents-&gt;IndexElementCount != storageContext-&gt;IndexElementCount)
    {
        hr = WINBIO_E_DATABASE_BAD_INDEX_VECTOR;
        goto cleanup;
    }

    if (RecordContents-&gt;IndexElementCount &gt; 0 &amp;&amp;
        !ARGUMENT_PRESENT(RecordContents-&gt;IndexVector))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Call a private function (_CheckForDuplicateEnrollments) to query the
    // database for existing records with the same identity and sub-factor 
    // values as the new record. If a duplicate is found, return.
    hr = _CheckForDuplicateEnrollments(
            Pipeline,
            RecordContents-&gt;Identity,
            RecordContents-&gt;SubFactor,
            &amp;duplicateRecordCount
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }
    if (duplicateRecordCount &gt; 0)
    {
        hr = WINBIO_E_DUPLICATE_ENROLLMENT;
        goto cleanup;
    }

    // Call a custom function (_EncryptTemplateData) to encrypt the template 
    // data. Do this now so that you can determine how much space will be 
    // required to store the encrypted template.
    hr = _EncryptTemplateData(
            &amp;storageContext-&gt;CryptoContext,
            RecordContents-&gt;TemplateBlob,
            RecordContents-&gt;TemplateBlobSize,
            &amp;encryptedTemplateBlob,
            &amp;encryptedTemplateBlobSize
            );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_WRITE_ERROR;
        goto cleanup;
    }

    // Call a custom function (_AllocateNewRecord) to allocate memory for the 
    // new record. You must allocate enough memory to hold the index vector, the
    // encrypted template, the identity structure, sub-factor information, and the 
    // payload blob. You must also allocate enough memory to hold and any other 
    // data that will be used by the storage adapter but that will
    // not be made visible to the engine adapter.
    hr = _AllocateNewRecord(
            RecordContents-&gt;IndexElementCount, 
            encryptedTemplateBlobSize,
            RecordContents-&gt;PayloadBlobSize,
            &amp;newRecord,                         // [out] Address of the new record buffer
            &amp;newRecordSize                      // [out] Size of the new record buffer
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Copy the identity information into the new record.
    CopyMemory(
        &amp;newRecord-&gt;Identity,
        RecordContents-&gt;Identity,
        sizeof(WINBIO_IDENTITY)
        );

    // Copy the sub-factor information to the new record.
    newRecord-&gt;SubFactor = RecordContents-&gt;SubFactor;

    // Copy the index vector, if present, into the new record.
    if (RecordContents-&gt;IndexElementCount &gt; 0)
    {
        PULONG indexVector = _GetIndexVector(newRecord);
        for (index=0; index &lt; RecordContents-&gt;IndexElementCount; ++index)
        {
            indexVector[index] = RecordContents-&gt;IndexVector[index];
        }
    }

    // Copy the encrypted template.
    templateBlobOffset = 
        sizeof(struct _MY_ADAPTER_RECORD_HEADER) + 
        RecordContents-&gt;IndexElementCount * sizeof(ULONG);

    newRecord-&gt;TemplateBlobSize = RecordContents-&gt;TemplateBlobSize;
    newRecord-&gt;EncryptedTemplateBlobSize = encryptedTemplateBlobSize;

    CopyMemory(
        (PUCHAR)newRecord + templateBlobOffset,
        encryptedTemplateBlob,
        encryptedTemplateBlobSize
        );
       
    // Copy the payload blob if present.
    if (RecordContents-&gt;PayloadBlobSize &gt; 0)
    {
        payloadBlobOffset =
            templateBlobOffset + 
            encryptedTemplateBlobSize;

        newRecord-&gt;PayloadBlobSize = RecordContents-&gt;PayloadBlobSize;

        CopyMemory(
            (PUCHAR)newRecord + payloadBlobOffset, 
            RecordContents-&gt;PayloadBlob, 
            RecordContents-&gt;PayloadBlobSize
            );
    }

    // Call a custom function (_LockDatabase) to lock the database for writing
    // (EXCLUSIVE ownership).
    hr = _LockDatabase(Pipeline-&gt;StorageHandle, TRUE);
    if (FAILED(hr))
    {
        goto cleanup;
    }
    lockAcquired = TRUE;

    // Call a custom function (_ReadFileHeader) to read the header block.
    hr = _ReadFileHeader( Pipeline-&gt;StorageHandle, &amp;fileHeader );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Write the new data record to the first free byte at the end of the
    // active data area in the database file.
    hr = _WriteRecord( 
            Pipeline-&gt;StorageHandle, 
            fileHeader.FirstFreeByte, 
            newRecord 
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Update the bookkeeping information in the header and write the header
    // back to the file.
    fileHeader.FirstFreeByte.QuadPart += newRecord-&gt;RecordSize;
    ++fileHeader.TotalRecordCount;

    hr = _WriteFileHeader(
            Pipeline-&gt;StorageHandle,
            &amp;fileHeader
            );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_CORRUPTED;
        goto cleanup;
    }

    // Recompute the file hash and write it to the protected data area in the database
    // file. The hash value is an integrity check on data stored in the file. Note that
    // the DPAPI-protected data block is NOT included in the hash.
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

    // Call the SecureZero function to overwrite the template encryption key 
    // on the stack.
    SecureZeroMemory( &amp;protectedData, sizeof(struct _MY_ADAPTER_DPAPI_DATA));

    if (lockAcquired == TRUE)
    {
        _UnlockDatabase( Pipeline-&gt;StorageHandle);
        lockAcquired = FALSE;
    }

    if (encryptedTemplateBlob != NULL)
    {
        SecureZeroMemory(encryptedTemplateBlob, encryptedTemplateBlobSize);
        _AdapterRelease(encryptedTemplateBlob);
        encryptedTemplateBlob = NULL;
    }

    if (newRecord != NULL)
    {
        SecureZeroMemory( newRecord, newRecordSize);
        _AdapterRelease(newRecord);
        newRecord = NULL;
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/f1939410-1c1e-42e4-98d6-d8866d313ca1">StorageAdapterDeleteRecord</a>
 

 

