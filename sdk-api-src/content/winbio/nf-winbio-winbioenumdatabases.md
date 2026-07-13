---
UID: NF:winbio.WinBioEnumDatabases
title: WinBioEnumDatabases function (winbio.h)
description: Enumerates all registered databases that match a specified type.
helpviewer_keywords: ["WinBioEnumDatabases","WinBioEnumDatabases function [Windows Biometric Framework API]","secbiomet.winbioenumdatabases","winbio/WinBioEnumDatabases"]
old-location: secbiomet\winbioenumdatabases.htm
tech.root: SecBioMet
ms.assetid: 163c669d-765f-4f8d-83c4-ff8bd064e44d
ms.date: 12/05/2018
ms.keywords: WinBioEnumDatabases, WinBioEnumDatabases function [Windows Biometric Framework API], secbiomet.winbioenumdatabases, winbio/WinBioEnumDatabases
req.header: winbio.h
req.include-header: Winbio.h
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
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WinBioEnumDatabases
 - winbio/WinBioEnumDatabases
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - winbioext.dll
 - Ext-MS-Win-BioMetrics-WinBio-L1-3-0.dll
api_name:
 - WinBioEnumDatabases
---

# WinBioEnumDatabases function


## -description

Enumerates all registered databases that match a specified type.

## -parameters

### -param Factor [in]

A bitmask of WINBIO_BIOMETRIC_TYPE flags that specifies the biometric unit types to be enumerated.  Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.

### -param StorageSchemaArray [out]

Address of a variable that receives a pointer to  an array of   <a href="/windows/desktop/SecBioMet/winbio-storage-schema">WINBIO_STORAGE_SCHEMA</a> structures that contain information about each database. If the function does not succeed, the pointer is set to <b>NULL</b>. If the function succeeds, you must pass the pointer to <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release memory allocated internally for the array.

### -param StorageCount [out]

Pointer to a value that specifies the number of structures pointed to by the <i>StorageSchemaArray</i> parameter.

## -returns

If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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
The bitmask contained in the <i>Factor</i> parameter contains one or more an invalid type bits.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to complete the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>StorageSchemaArray</i> and <i>StorageCount</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported in the <i>Factor</i> parameter.

If information about multiple databases is returned in the array of structures pointed to by the <i>StorageSchemaArray</i> parameter, the databases are not guaranteed to be in any particular order.

After you are finished using the structures returned to the <i>StorageSchemaArray</i> parameter, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory allocated internally for the array.


#### Examples

The following code example calls <b>WinBioEnumDatabases</b> to enumerate the
biometric databases on the system. The example also includes a function, DisplayGuid, to display the database ID. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT EnumDatabases( )
{
    // Declare variables.
    HRESULT hr = S_OK;
    PWINBIO_STORAGE_SCHEMA storageSchemaArray = NULL;
    SIZE_T storageCount = 0;
    SIZE_T index = 0;

    // Enumerate the databases.
    hr = WinBioEnumDatabases( 
            WINBIO_TYPE_FINGERPRINT,    // Type of biometric unit
            &storageSchemaArray,        // Array of database schemas
            &storageCount );            // Number of database schemas
    if (FAILED(hr))
    {
        wprintf_s(L"\nWinBioEnumDatabases failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Display information for each database.
    wprintf_s(L"\nDatabases:\n");
    for (index = 0; index < storageCount; ++index)
    {
        wprintf_s(L"\n[%d]: \tBiometric factor: 0x%08x\n", 
                 index, 
                 storageSchemaArray[index].BiometricFactor );
        
        wprintf_s(L"\tDatabase ID: ");
        DisplayGuid(&storageSchemaArray[index].DatabaseId);
        wprintf_s(L"\n");

        wprintf_s(L"\tData format: ");
        DisplayGuid(&storageSchemaArray[index].DataFormat);
        wprintf_s(L"\n");

        wprintf_s(L"\tAttributes:  0x%08x\n", 
                 storageSchemaArray[index].Attributes);

        wprintf_s(L"\tFile path:   %ws\n", 
                 storageSchemaArray[index].FilePath );

        wprintf_s(L"\tCnx string:  %ws\n", 
                 storageSchemaArray[index].ConnectionString );

        wprintf_s(L"\n");
    }

e_Exit:
    if (storageSchemaArray != NULL)
    {
        WinBioFree(storageSchemaArray);
        storageSchemaArray = NULL;
    }

    wprintf_s(L"\nPress any key to exit...");
    _getch();

    return hr;
}


//------------------------------------------------------------------------
// The following function displays a GUID to the console window.
//
VOID DisplayGuid( __in PWINBIO_UUID Guid )
{
    wprintf_s(
        L"{%08X-%04X-%04X-%02X%02X-%02X%02X%02X%02X%02X%02X}",
        Guid->Data1,
        Guid->Data2,
        Guid->Data3,
        Guid->Data4[0],
        Guid->Data4[1],
        Guid->Data4[2],
        Guid->Data4[3],
        Guid->Data4[4],
        Guid->Data4[5],
        Guid->Data4[6],
        Guid->Data4[7]
        );
}


```

## -see-also

<a href="/windows/desktop/SecBioMet/winbio-storage-schema">WINBIO_STORAGE_SCHEMA</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumserviceproviders">WinBioEnumServiceProviders</a>