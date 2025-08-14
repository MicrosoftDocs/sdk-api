---
UID: NF:winbio.WinBioEnumBiometricUnits
title: WinBioEnumBiometricUnits function (winbio.h)
description: Enumerates all attached biometric units that match the input type.
old-location: secbiomet\winbioenumbiometricunits.htm
tech.root: SecBioMet
ms.assetid: e1ca5712-978e-4e31-a941-eb462c670eac
ms.date: 12/05/2018
ms.keywords: WinBioEnumBiometricUnits, WinBioEnumBiometricUnits function [Windows Biometric Framework API], secbiomet.winbioenumbiometricunits, winbio/WinBioEnumBiometricUnits
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
 - WinBioEnumBiometricUnits
 - winbio/WinBioEnumBiometricUnits
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
 - WinBioEnumBiometricUnits
---

# WinBioEnumBiometricUnits function


## -description

Enumerates all attached biometric units that match the input type.

## -parameters

### -param Factor [in]

A bitmask of WINBIO_BIOMETRIC_TYPE flags that specifies the biometric unit types to be enumerated. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.

### -param UnitSchemaArray [out]

Address of a variable that receives a pointer to an array of   <a href="/windows/desktop/SecBioMet/winbio-unit-schema">WINBIO_UNIT_SCHEMA</a> structures that contain information about each enumerated biometric unit. If the function does not succeed, the pointer is set to <b>NULL</b>. If the function succeeds, you must pass the pointer to <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release memory allocated internally for the array.

### -param UnitCount [out]

Pointer to a value that specifies the number of structures pointed to by the <i>UnitSchemaArray</i> parameter.

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
The <i>UnitSchemaArray</i> and <i>UnitCount</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_DISABLED</b></b></dt>
</dl>
</td>
<td width="60%">
Current administrative policy prohibits use of the Windows Biometric Framework API.

</td>
</tr>
</table>

## -remarks

Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported in the <i>Factor</i> parameter.

If information about multiple installed biometric units is returned in the array of structures pointed to by the <i>UnitSchemaArray</i> parameter, the units are not guaranteed to be in any particular order.

After you are finished using the structures returned to the <i>UnitSchemaArray</i> parameter, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory allocated internally for the array.

If all of the factor bits in the <i>Factor</i> bitmask refer to unsupported biometric types, the function returns S_OK but the value pointed to by the <i>UnitSchemaArray</i> parameter will be NULL and the <i>UnitCount</i> parameter will contain zero. Although it is not an error to inquire about unsupported biometric factors, the result of the query will be an empty set.


#### Examples

The following function calls <b>WinBioEnumBiometricUnits</b> to enumerate the installed biometric units. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT EnumerateSensors( )
{
    // Declare variables.
    HRESULT hr = S_OK;
    PWINBIO_UNIT_SCHEMA unitSchema = NULL;
    SIZE_T unitCount = 0;
    SIZE_T index = 0;

    // Enumerate the installed biometric units.
    hr = WinBioEnumBiometricUnits( 
            WINBIO_TYPE_FINGERPRINT,        // Type of biometric unit
            &unitSchema,                    // Array of unit schemas
            &unitCount );                   // Count of unit schemas

    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Display information for each installed biometric unit.
    wprintf_s(L"\nSensors: \n");
    for (index = 0; index < unitCount; ++index)
    {
        wprintf_s(L"\n[%d]: \tUnit ID: %d\n", 
                 index, 
                 unitSchema[index].UnitId );
        wprintf_s(L"\tDevice instance ID: %s\n", 
                 unitSchema[index].DeviceInstanceId );
        wprintf_s(L"\tPool type: %d\n", 
                 unitSchema[index].PoolType );
        wprintf_s(L"\tBiometric factor: %d\n", 
                 unitSchema[index].BiometricFactor );
        wprintf_s(L"\tSensor subtype: %d\n", 
                 unitSchema[index].SensorSubType );
        wprintf_s(L"\tSensor capabilities: 0x%08x\n", 
                 unitSchema[index].Capabilities );
        wprintf_s(L"\tDescription: %s\n", 
                 unitSchema[index].Description );
        wprintf_s(L"\tManufacturer: %s\n", 
                 unitSchema[index].Manufacturer );
        wprintf_s(L"\tModel: %s\n", 
                 unitSchema[index].Model );
        wprintf_s(L"\tSerial no: %s\n", 
                 unitSchema[index].SerialNumber );
        wprintf_s(L"\tFirmware version: [%d.%d]\n", 
                 unitSchema[index].FirmwareVersion.MajorVersion, 
                 unitSchema[index].FirmwareVersion.MinorVersion);
    }


e_Exit:
    if (unitSchema != NULL)
    {
        WinBioFree(unitSchema);
        unitSchema = NULL;
    }

    wprintf_s(L"\nPress any key to exit...");
    _getch();

    return hr;
}


```

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumdatabases">WinBioEnumDatabases</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumserviceproviders">WinBioEnumServiceProviders</a>