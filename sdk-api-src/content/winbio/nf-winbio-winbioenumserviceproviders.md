---
UID: NF:winbio.WinBioEnumServiceProviders
title: WinBioEnumServiceProviders function (winbio.h)
description: Retrieves information about installed biometric service providers. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbioenumserviceproviders.htm
tech.root: SecBioMet
ms.assetid: 2424eae8-4fc6-43f4-97a1-3340870396cc
ms.date: 12/05/2018
ms.keywords: WinBioEnumServiceProviders, WinBioEnumServiceProviders function [Windows Biometric Framework API], secbiomet.winbioenumserviceproviders, winbio/WinBioEnumServiceProviders
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
 - WinBioEnumServiceProviders
 - winbio/WinBioEnumServiceProviders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-biometrics-winbio-core-l1-1-6.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-5.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-4.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-3.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-2.dll
 - Winbio.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioEnumServiceProviders
---

# WinBioEnumServiceProviders function


## -description

Retrieves information about installed biometric service providers. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param Factor [in]

A bitmask of WINBIO_BIOMETRIC_TYPE flags that specifies the biometric unit types to be enumerated. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.

### -param BspSchemaArray [out]

Address of a variable that receives a pointer  to an array of <a href="/windows/desktop/SecBioMet/winbio-bsp-schema">WINBIO_BSP_SCHEMA</a> structures that contain information about each of the available service providers.  If the function does not succeed, the pointer is set to <b>NULL</b>. If the function succeeds, you must pass the pointer to <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release memory allocated internally for the array.

### -param BspCount [out]

Pointer to a value that specifies the number of structures pointed to by the <i>BspSchemaArray</i> parameter.

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
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>BspSchemaArray</i> and <i>BspCount</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported in the <i>Factor</i> parameter.

After you are finished using the structures returned to the <i>BspSchemaArray</i> parameter, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory allocated internally for the array.

If all of the factor bits in the <i>Factor</i> bitmask refer to unsupported biometric types, the function returns S_OK but the value pointed to by the <i>BspSchemaArray</i> parameter will be <b>NULL</b> and the <i>BspCount</i> parameter will contain zero. Although it is not an error to inquire about unsupported biometric factors, the result of the query will be an empty set.


#### Examples

The following code example calls <b>WinBioEnumServiceProviders</b> to enumerate
the installed service providers. The example also includes a function, DisplayGuid, to display the provider ID. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT EnumSvcProviders( )
{
    // Declare variables.
    HRESULT hr = S_OK;
    PWINBIO_BSP_SCHEMA bspSchemaArray = NULL;
    SIZE_T bspCount = 0;
    SIZE_T index = 0;

    // Enumerate the service providers.
    hr = WinBioEnumServiceProviders( 
            WINBIO_TYPE_FINGERPRINT,    // Provider to enumerate
            &bspSchemaArray,            // Provider schema array
            &bspCount );                // Number of schemas returned
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumServiceProviders failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Display the schema information.
    wprintf_s(L"\nService providers: \n");
    for (index = 0; index < bspCount; ++index)
    {
        wprintf_s(L"\n[%d]: \tBiometric factor: 0x%08x\n", 
                 index, 
                 bspSchemaArray[index].BiometricFactor );
        
        wprintf_s(L"\tBspId: ");
        DisplayGuid(&bspSchemaArray[index].BspId);
        wprintf_s(L"\n");

        wprintf_s(L"\tDescription: %ws\n", 
                 bspSchemaArray[index].Description);
        wprintf_s(L"\tVendor: %ws\n", 
                 bspSchemaArray[index].Vendor );
        wprintf_s(L"\tVersion: %d.%d\n", 
                 bspSchemaArray[index].Version.MajorVersion, 
                 bspSchemaArray[index].Version.MinorVersion);

        wprintf_s(L"\n");
    } 

e_Exit:
    if (bspSchemaArray != NULL)
    {
        WinBioFree(bspSchemaArray);
        bspSchemaArray = NULL;
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

<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumdatabases">WinBioEnumDatabases</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>