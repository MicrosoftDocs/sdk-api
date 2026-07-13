---
UID: NF:winbio.WinBioFree
title: WinBioFree function (winbio.h)
description: Releases memory allocated for the client application by an earlier call to a Windows Biometric Framework API function. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioFree","WinBioFree function [Windows Biometric Framework API]","secbiomet.winbiofree","winbio/WinBioFree"]
old-location: secbiomet\winbiofree.htm
tech.root: SecBioMet
ms.assetid: b570fc6c-a08e-4485-a621-20f59bd63d40
ms.date: 12/05/2018
ms.keywords: WinBioFree, WinBioFree function [Windows Biometric Framework API], secbiomet.winbiofree, winbio/WinBioFree
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
 - WinBioFree
 - winbio/WinBioFree
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
 - WinBioFree
---

# WinBioFree function


## -description

Releases memory allocated for the client application by an earlier call to a Windows Biometric Framework API function.  Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param Address [in]

Address of the memory block to delete.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Address</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Multiple functions in the Windows Biometric Framework API allocate memory for the client application and pass the address of that memory to the client. To prevent memory leaks, you must call <b>WinBioFree</b> to delete the block when you are done using the information it contains. You delete the memory by passing its address to <b>WinBioFree</b>. You can find the address by de-referencing the pointer specified by the appropriate parameter in each of the following functions.

<table>
<tr>
<th>Function</th>
<th>Parameter</th>
<th>Type of block allocated</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>
</td>
<td><i>Sample</i></td>
<td>Structure</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a>
</td>
<td><i>UnitSchemaArray</i></td>
<td>Array of structures</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumdatabases">WinBioEnumDatabases</a>
</td>
<td><i>StorageSchemaArray</i></td>
<td>Array of structures</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>
</td>
<td><i>SubFactorArray</i></td>
<td>Array of integers</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumserviceproviders">WinBioEnumServiceProviders</a>
</td>
<td><i>BspSchemaArray</i></td>
<td>Array of structures</td>
</tr>
<tr>
<td>EventCallBack</td>
<td><i>Event</i></td>
<td>Structure</td>
</tr>
<tr>
<td>CaptureCallback</td>
<td><i>Sample</i></td>
<td>Structure</td>
</tr>
</table>
 


#### Examples

The following function calls <a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a> to enumerate
the installed biometric sensors, and it calls <b>WinBioFree</b> to release the
memory created by <b>WinBioEnumBiometricUnits</b>. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT EnumerateSensors( )
{
    HRESULT hr = S_OK;
    PWINBIO_UNIT_SCHEMA unitSchema = NULL;
    SIZE_T unitCount = 0;

    // Enumerate the installed biometric units.
    hr = WinBioEnumBiometricUnits( 
            WINBIO_TYPE_FINGERPRINT,        // Type of biometric unit
            &unitSchema,                    // Array of unit schemas
            &unitCount );                   // Count of unit schemas

    if (FAILED(hr))
    {
        wprintf_s(L"\nWinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

e_Exit:

    // Free memory.
    if (unitSchema != NULL)
    {
        WinBioFree(unitSchema);
        unitSchema = NULL;
    }

    return hr;
}


```

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumdatabases">WinBioEnumDatabases</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumenrollments">WinBioEnumEnrollments</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumserviceproviders">WinBioEnumServiceProviders</a>