---
UID: NC:winbio_adapter.PIBIO_STORAGE_QUERY_BY_CONTENT_FN
title: PIBIO_STORAGE_QUERY_BY_CONTENT_FN
author: windows-sdk-content
description: Queries the database that is currently open for templates associated with a specified index vector.
old-location: secbiomet\storageadapterquerybycontent.htm
old-project: SecBioMet
ms.assetid: 773aacd1-a34a-4c5a-b615-2a5485f13ca1
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: PIBIO_STORAGE_QUERY_BY_CONTENT_FN, PIBIO_STORAGE_QUERY_BY_CONTENT_FN callback, StorageAdapterQueryByContent, StorageAdapterQueryByContent callback function [Windows Biometric Framework API], secbiomet.storageadapterquerybycontent, winbio_adapter/StorageAdapterQueryByContent
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
tech.root: 
req.typenames: WINBIO_ASYNC_RESULT, *PWINBIO_ASYNC_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Winbio_adapter.h
api_name:
-	StorageAdapterQueryByContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PIBIO_STORAGE_QUERY_BY_CONTENT_FN callback function


## -description


Called by the engine adapter to locate templates that match a specified index vector.



## -parameters




### -param Pipeline [in, out]

Pointer to the  <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.



### -param SubFactor [in]

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that specifies the sub-factor associated with the template.


### -param IndexVector[]


### -param IndexElementCount [in]

A value that contains the number of elements in the index vector array. This must match the size specified when the database was created. If the database was created with a zero length index, this parameter must be zero.



#### - IndexVector [in]

Pointer to an array of <b>ULONG</b> index values. Any template that has a matching index will be returned. If the database was created with a zero length index, this parameter must be <b>NULL</b>.


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
The argument specified by the <i>SubFactor</i> parameter is not valid.

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
<dt><b><b>WINBIO_E_DATABASE_BAD_INDEX_VECTOR</b></b></dt>
</dl>
</td>
<td width="60%">
The size of the  index vector does not match the index size specified when the database was created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DATABASE_NO_RESULTS</b></b></dt>
</dl>
</td>
<td width="60%">
The query was successful, but no matching records could be found.

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
<dt><b><b>WINBIO_E_DATABASE_READ_ERROR</b></b></dt>
</dl>
</td>
<td width="60%">
An unspecified problem occurred.

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



If this method returns successfully, the result set in the pipeline is replaced by the results of the query even if the query returns an empty set.

If the database was created with a zero length index vector, the result set will contain every record for which the template sub factor matches the <i>SubFactor</i> parameter. In that case, if the caller passes WINBIO_SUBTYPE_ANY for the <i>SubFactor</i> parameter, this function returns all records in the database.

After a successful call to this function, the result set cursor should be  positioned on the first record in the set.

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
// StorageAdapterQueryByContent
//
// Purpose:
//      Locates templates that match a specified index vector.
//
// Parameters:
//      Pipeline          - Pointer to a WINBIO_PIPELINE structure associated with 
//                          the biometric unit performing the operation.
//      SubFactor         - A WINBIO_BIOMETRIC_SUBTYPE value that specifies the sub-factor 
//                          associated with the template.
//      IndexVector       - Pointer to an array of ULONG index values.
//      IndexElementCount - A value that contains the number of elements in the index 
//                          vector array.
//
static HRESULT
WINAPI
StorageAdapterQueryByContent(
    __inout PWINBIO_PIPELINE Pipeline,
    __in WINBIO_BIOMETRIC_SUBTYPE SubFactor,
    __in ULONG IndexVector[],
    __in SIZE_T IndexElementCount
    )
{
    HRESULT hr = S_OK;
    BOOL lockAcquired = FALSE;
    struct _MY_ADAPTER_FILE_HEADER fileHeader = {0};
    SIZE_T remainingRecords = 0;
    LARGE_INTEGER currentRecordOffset = {0};
    struct _MY_ADAPTER_RECORD_HEADER *recordHeader = NULL;
    SIZE_T recordHeaderSize = 0;

    // Verify that the Pipeline parameter is not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(IndexVector))
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

    // WINBIO_SUBTYPE_ANY is a valid sub-factor.
    // WINBIO_SUBTYPE_NO_INFORMATION is not a valid sub-factor.
    if (SubFactor == WINBIO_SUBTYPE_NO_INFORMATION)
    {
        hr = E_INVALIDARG;
        goto cleanup;
    }

    // Validate the IndexElementCount argument.
    if (IndexElementCount != storageContext-&gt;IndexElementCount)
    {
        hr = WINBIO_E_DATABASE_BAD_INDEX_VECTOR;
        goto cleanup;
    }
    if (storageContext-&gt;IndexElementCount &gt; 0 &amp;&amp;
        !ARGUMENT_PRESENT(IndexVector))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Clear the result set.
    hr = StorageAdapterClearContext(Pipeline);
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Lock the database for reading.
    hr = _LockDatabase( Pipeline-&gt;StorageHandle, FALSE);
    if (FAILED(hr))
    {
        goto cleanup;
    }
    lockAcquired = TRUE;

    // Read the header block.
    hr = _ReadFileHeader( Pipeline-&gt;StorageHandle, &amp;fileHeader );
    if (FAILED(hr))
    {
        goto cleanup;
    }

    // Scan through all records looking for index vector matches.
    recordHeaderSize = 
        sizeof(struct _MY_ADAPTER_RECORD_HEADER) +
        (SIZE_T)fileHeader.IndexElementCount * sizeof(ULONG);

    currentRecordOffset = _MY_ADAPTER_FIRST_RECORD_OFFSET;
    remainingRecords = fileHeader.TotalRecordCount;

    while (remainingRecords &gt; 0)
    {
        SIZE_T recordSize = 0;
        BOOLEAN match = FALSE;
        LARGE_INTEGER dataOffset = {0};

        // If you did not give up the current header during the previous 
        // iteration of the loop, reuse it.
        if (recordHeader == NULL)
        {
            recordHeader = (struct _MY_ADAPTER_RECORD_HEADER*)_AdapterAlloc( recordHeaderSize );
            if (recordHeader == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto cleanup;
            }
        }
        else
        {
            ZeroMemory(recordHeader, recordHeaderSize);
        }

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

        // Skip records marked for deletion.
        if ((recordHeader-&gt;Flags &amp; _MY_ADAPTER_FLAG_RECORD_DELETED) == 0)
        {
            // Call a custom function (_MatchIndexVector) that compares the index
            // vector of the current record with the input index vector.
            hr = _MatchIndexVector(
                    SubFactor,
                    IndexVector,
                    IndexElementCount,
                    recordHeader-&gt;SubFactor,
                    _GetIndexVector(recordHeader),
                    storageContext-&gt;IndexElementCount,
                    &amp;match
                    );
            if (FAILED(hr))
            {
                goto cleanup;
            }

            if (match == TRUE)
            {
                // Calculate the file offset of this record's data area.
                dataOffset.QuadPart = 
                    currentRecordOffset.QuadPart + 
                    recordHeader-&gt;RecordHeaderSize;

                // Add the matching record to the result set in the pipeline.
                hr = _ResultSetAddElement( 
                        &amp;storageContext-&gt;ResultSet, 
                        recordHeader, 
                        dataOffset
                        );
                if (FAILED(hr))
                {
                    goto cleanup;
                }
                // The result set now owns the record header. Set the pointer
                // to NULL.
                recordHeader = NULL;
            }
        }

        currentRecordOffset.QuadPart += recordSize;
        --remainingRecords;
    }

    // If the search was successful, but the result set is empty, return 
    // WINBIO_E_DATABASE_NO_RESULTS
    if (SUCCEEDED(hr))
    {
        SIZE_T elementCount = 0;
        hr = _ResultSetGetCount(&amp;storageContext-&gt;ResultSet, &amp;elementCount);
    }

cleanup:

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

    if (FAILED(hr))
    {
        // Clear any partial result set from the pipeline.
        StorageAdapterClearContext(Pipeline);
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/736688c3-2c2c-4244-9f49-98ad0fe2d141">StorageAdapterFirstRecord</a>



<a href="https://msdn.microsoft.com/a06550da-c6ea-44e5-b54f-8005bcbc0364">StorageAdapterGetCurrentRecord</a>



<a href="https://msdn.microsoft.com/dc7891c3-33f7-498c-acb1-4687909debb7">StorageAdapterGetRecordCount</a>



<a href="https://msdn.microsoft.com/e0025167-0778-474e-baca-ffc767822893">StorageAdapterNextRecord</a>



<a href="https://msdn.microsoft.com/b2c93122-fae1-44ad-97d4-f90115194a31">StorageAdapterQueryBySubject</a>
 

 

