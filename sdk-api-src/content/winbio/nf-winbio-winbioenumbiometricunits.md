---
UID: NF:winbio.WinBioEnumBiometricUnits
title: WinBioEnumBiometricUnits function
author: windows-sdk-content
description: Enumerates all attached biometric units that match the input type.
old-location: secbiomet\winbioenumbiometricunits.htm
old-project: SecBioMet
ms.assetid: e1ca5712-978e-4e31-a941-eb462c670eac
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: WinBioEnumBiometricUnits, WinBioEnumBiometricUnits function [Windows Biometric Framework API], secbiomet.winbioenumbiometricunits, winbio/WinBioEnumBiometricUnits
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winbio.dll
-	ext-ms-win-biometrics-winbio-core-l1-1-0.dll
-	Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
-	WinBioEnumBiometricUnits
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioEnumBiometricUnits function


## -description


Enumerates all attached biometric units that match the input type.


## -parameters




### -param Factor [in]

A bitmask of WINBIO_BIOMETRIC_TYPE flags that specifies the biometric unit types to be enumerated. Only <b>WINBIO_TYPE_FINGERPRINT</b> is currently supported.


### -param UnitSchemaArray [out]

Address of a variable that receives a pointer to an array of   <a href="https://msdn.microsoft.com/b20adf18-2948-481f-9d12-8da17aa152f7">WINBIO_UNIT_SCHEMA</a> structures that contain information about each enumerated biometric unit. If the function does not succeed, the pointer is set to <b>NULL</b>. If the function succeeds, you must pass the pointer to <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release memory allocated internally for the array.


### -param UnitCount [out]

Pointer to a value that specifies the number of structures pointed to by the <i>UnitSchemaArray</i> parameter.


## -returns



If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

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

After you are finished using the structures returned to the <i>UnitSchemaArray</i> parameter, you must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the memory allocated internally for the array.

If all of the factor bits in the <i>Factor</i> bitmask refer to unsupported biometric types, the function returns S_OK but the value pointed to by the <i>UnitSchemaArray</i> parameter will be NULL and the <i>UnitCount</i> parameter will contain zero. Although it is not an error to inquire about unsupported biometric factors, the result of the query will be an empty set.


#### Examples

The following function calls <b>WinBioEnumBiometricUnits</b> to enumerate the installed biometric units. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumerateSensors( )
{
    // Declare variables.
    HRESULT hr = S_OK;
    PWINBIO_UNIT_SCHEMA unitSchema = NULL;
    SIZE_T unitCount = 0;
    SIZE_T index = 0;

    // Enumerate the installed biometric units.
    hr = WinBioEnumBiometricUnits( 
            WINBIO_TYPE_FINGERPRINT,        // Type of biometric unit
            &amp;unitSchema,                    // Array of unit schemas
            &amp;unitCount );                   // Count of unit schemas

    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Display information for each installed biometric unit.
    wprintf_s(L"\nSensors: \n");
    for (index = 0; index &lt; unitCount; ++index)
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

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/163c669d-765f-4f8d-83c4-ff8bd064e44d">WinBioEnumDatabases</a>



<a href="https://msdn.microsoft.com/bd5fd36a-ed90-4dd0-8a84-0412544493dd">WinBioEnumEnrollments</a>



<a href="https://msdn.microsoft.com/2424eae8-4fc6-43f4-97a1-3340870396cc">WinBioEnumServiceProviders</a>
 

 

