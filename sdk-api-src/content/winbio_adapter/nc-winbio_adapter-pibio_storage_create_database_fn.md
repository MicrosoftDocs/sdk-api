---
UID: NC:winbio_adapter.PIBIO_STORAGE_CREATE_DATABASE_FN
title: PIBIO_STORAGE_CREATE_DATABASE_FN
author: windows-sdk-content
description: Creates and configures a new database.
old-location: secbiomet\storageadaptercreatedatabase.htm
tech.root: SecBioMet
ms.assetid: 7b9e034e-51d4-4209-9092-14e21e9fff3c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PIBIO_STORAGE_CREATE_DATABASE_FN, PIBIO_STORAGE_CREATE_DATABASE_FN callback, StorageAdapterCreateDatabase, StorageAdapterCreateDatabase callback function [Windows Biometric Framework API], secbiomet.storageadaptercreatedatabase, winbio_adapter/StorageAdapterCreateDatabase
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
 - StorageAdapterCreateDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PIBIO_STORAGE_CREATE_DATABASE_FN callback function


## -description


Called by the Windows Biometric Framework to create and configure a new database.


## -parameters




### -param Pipeline [in, out]

Pointer to a <a href="https://msdn.microsoft.com/b5fc2b14-b0b6-4327-a42a-ecae41c3e12a">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.


### -param DatabaseId [in]

Pointer to a GUID that uniquely identifies the database. This is the same GUID used to register the database in the registry.


### -param Factor [in]

A WINBIO_BIOMETRIC_TYPE value that specifies the type of the biometric factor stored in this database. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.


### -param Format [in]

Pointer to a GUID that specifies the vendor-defined format of the data in the <b>VendorDataBlock</b> member of the <a href="https://msdn.microsoft.com/39cfab34-0416-4897-bf95-a1b3c3a6a7a1">WINBIO_BIR</a> object.


### -param FilePath [in]

Pointer to a <b>NULL</b>-terminated Unicode string that contains the fully qualified file path for the database.


### -param ConnectString [in]

Pointer to a <b>NULL</b>-terminated Unicode connection string for the database.


### -param IndexElementCount [in]

The number of elements in the index vector. This can be equal to or greater than zero.


### -param InitialSize [in]

A value that contains the beginning size of the  database, in bytes.


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
<dt><b>WINBIO_E_INVALID_DEVICE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>StorageContext</b> member of the pipeline object is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The biometric service calls this method if the <a href="https://msdn.microsoft.com/4f3dfa67-5020-461a-b3d1-33c948129bdf">StorageAdapterOpenDatabase</a> function fails and if an <b>AutoCreate</b> flag has been associated with the database in the registry.

If this function succeeds, the database must be left in the open state. The Windows Biometric Framework will not issue a subsequent call to this function.



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
// StorageAdapterCreateDatabase
//
// Purpose:
//      Creates and configures a new database.
//
// Parameters:
//      Pipeline          - Pointer to a WINBIO_PIPELINE structure associated with 
//                          the biometric unit performing the operation.
//      DatabaseId        - Pointer to a GUID that uniquely identifies the database.
//      Factor            - A WINBIO_BIOMETRIC_TYPE value that specifies the type 
//                          of the biometric factor stored in the database.
//      Format            - Pointer to a GUID that specifies the vendor-defined format
//                          of the data
//      FilePath          - Pointer to the database file path.
//      ConnectString     - Pointer to the database connection string.
//      IndexElementCount - Number of elements in the index vector.
//      InitialSize       - Beginning size of the database, in bytes.
//
// Note:
//      The following example assumes that the database file has the following format:
//
//          [protected area]
//          [header]
//          [record 0]
//          [record 1]
//              .
//              .
//              .
//          [record N]
//
//      It is the responsibility of the storage adapter writer to implement protection
//      and to determine how and where encryption keys are stored.
//
static HRESULT
WINAPI
StorageAdapterCreateDatabase(
    __inout PWINBIO_PIPELINE Pipeline,
    __in PWINBIO_UUID DatabaseId,
    __in WINBIO_BIOMETRIC_TYPE Factor,
    __in PWINBIO_UUID Format,
    __in LPCWSTR FilePath,
    __in LPCWSTR ConnectString,
    __in SIZE_T IndexElementCount,
    __in SIZE_T InitialSize
    )
{
    UNREFERENCED_PARAMETER(InitialSize);

    HRESULT hr = S_OK;
    struct _MY_ADAPTER_FILE_HEADER fileHeader = {0};
    BOOL fileOpen = FALSE;
    HANDLE fileHandle = INVALID_HANDLE_VALUE;
    struct _MY_ADAPTER_DPAPI_DATA protectedData = {0};
 
    // Verify that pointer arguments are not NULL.
    if (!ARGUMENT_PRESENT(Pipeline) ||
        !ARGUMENT_PRESENT(DatabaseId) ||
        !ARGUMENT_PRESENT(Format) ||
        !ARGUMENT_PRESENT(FilePath) ||
        !ARGUMENT_PRESENT(ConnectString))
    {
        hr = E_POINTER;
        goto cleanup;
    }

    // Retrieve the context from the pipeline.
    PWINBIO_STORAGE_CONTEXT storageContext = 
           (PWINBIO_STORAGE_CONTEXT)Pipeline-&gt;StorageContext;

    // Verify the pipeline state.
    if (storageContext == NULL ||
        Pipeline-&gt;StorageHandle != INVALID_HANDLE_VALUE)
    {
        hr = WINBIO_E_INVALID_DEVICE_STATE;
        goto cleanup;
    }

    // Call a custom function (_InitializeFileHeader) to copy database 
    // attributes into a structure to be used by the file management routines
    // in the adapter.
    hr = _InitializeFileHeader(
            DatabaseId,
            Factor,
            Format,
            IndexElementCount,
            &amp;fileHeader
            );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_CANT_CREATE;
        goto cleanup;
    }

    // Call a custom file management function (_CreateDatabase) to create
    // and open the database. Because the database is new, this function 
    // should generate a random key that can be used to encrypt and 
    // decrypt biometric templates stored in the database. The key should be
    // saved in the protected data area of the file. We recommend that you
    // encrypt the key by using the Data Protection API (DPAPI).
    hr = _CreateDatabase(
            &amp;fileHeader,
            FilePath,
            &amp;fileHandle,
            &amp;protectedData
            );
    if (FAILED(hr))
    {
        goto cleanup;
    }
    fileOpen = TRUE;


    // Call a custom function (_InitializeCryptoContext) to extract the template
    // decryption key from the protected block of the database and use other
    // appropriate values from that block as necessary to set up CNG cryptography 
    // algorithms. This function should associate the CNG cryptography handles 
    // with the storage context.
    hr = _InitializeCryptoContext(
            &amp;protectedData,
            &amp;storageContext-&gt;CryptoContext
            );
    if (FAILED(hr))
    {
        hr = WINBIO_E_DATABASE_CANT_CREATE;
        goto cleanup;
    }

    // Attach the database file handle to the pipeline.
    Pipeline-&gt;StorageHandle = fileHandle;
    fileHandle = INVALID_HANDLE_VALUE;

    // Copy various database parameters to the storage context. The following 
    // example code assumes that the context contains fields for the following
    // items:
    //      - Number of index elements
    //      - File version number
    //      - Template format
    //      - Database ID 
    //      - Database file path
    storageContext-&gt;IndexElementCount = IndexElementCount;

    CopyMemory( 
        &amp;storageContext-&gt;TemplateFormat, 
        &amp;fileHeader.TemplateFormat, 
        sizeof(WINBIO_UUID)
        );

    storageContext-&gt;Version = fileHeader.Version;

    CopyMemory(
        &amp;storageContext-&gt;DatabaseId,
        DatabaseId,
        sizeof(WINBIO_UUID)
        );

    wcsncpy_s(
        storageContext-&gt;FilePath,
        MAX_PATH+1,
        FilePath,
        MAX_PATH
        );

    // TODO: Copy other values as necessary to the storage context (not shown).

cleanup:

    if (FAILED(hr))
    {
        _CleanupCryptoContext(&amp;storageContext-&gt;CryptoContext);

        if (fileOpen)
        {
            CloseHandle(fileHandle);
            fileHandle = INVALID_HANDLE_VALUE;
        }
    }

    // Call the SecureZeroMemory function to overwrite the template encryption key 
    // on the stack.
    SecureZeroMemory( &amp;protectedData, sizeof(struct _MY_ADAPTER_DPAPI_DATA));

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/ddb8d0b8-e975-4ee2-bb8c-423b1304c467">StorageAdapterCloseDatabase</a>



<a href="https://msdn.microsoft.com/c1fc2f3f-034b-4546-aeee-1d1a38695793">StorageAdapterEraseDatabase</a>



<a href="https://msdn.microsoft.com/4f3dfa67-5020-461a-b3d1-33c948129bdf">StorageAdapterOpenDatabase</a>
 

 

