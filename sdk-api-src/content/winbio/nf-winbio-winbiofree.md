---
UID: NF:winbio.WinBioFree
title: WinBioFree function
author: windows-sdk-content
description: Releases memory allocated for the client application by an earlier call to a Windows Biometric Framework API function. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbiofree.htm
old-project: secbiomet
ms.assetid: b570fc6c-a08e-4485-a621-20f59bd63d40
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: WinBioFree, WinBioFree function [Windows Biometric Framework API], secbiomet.winbiofree, winbio/WinBioFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbio.h
req.include-header: Winbio.h
req.redist: 
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
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioFree
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioFree function


## -description


Releases memory allocated for the client application by an earlier call to a Windows Biometric Framework API function.  Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param Address [in]

Address of the memory block to delete.


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
<dt><b><b>E_POINTER</b></b></dt>
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
<a href="https://msdn.microsoft.com/365dcefb-3382-4b62-b47d-919e2d3f56f1">WinBioCaptureSample</a>
</td>
<td><i>Sample</i></td>
<td>Structure</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e1ca5712-978e-4e31-a941-eb462c670eac">WinBioEnumBiometricUnits</a>
</td>
<td><i>UnitSchemaArray</i></td>
<td>Array of structures</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/163c669d-765f-4f8d-83c4-ff8bd064e44d">WinBioEnumDatabases</a>
</td>
<td><i>StorageSchemaArray</i></td>
<td>Array of structures</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bd5fd36a-ed90-4dd0-8a84-0412544493dd">WinBioEnumEnrollments</a>
</td>
<td><i>SubFactorArray</i></td>
<td>Array of integers</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2424eae8-4fc6-43f4-97a1-3340870396cc">WinBioEnumServiceProviders</a>
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

The following function calls <a href="https://msdn.microsoft.com/e1ca5712-978e-4e31-a941-eb462c670eac">WinBioEnumBiometricUnits</a> to enumerate
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




<a href="https://msdn.microsoft.com/365dcefb-3382-4b62-b47d-919e2d3f56f1">WinBioCaptureSample</a>



<a href="https://msdn.microsoft.com/e1ca5712-978e-4e31-a941-eb462c670eac">WinBioEnumBiometricUnits</a>



<a href="https://msdn.microsoft.com/163c669d-765f-4f8d-83c4-ff8bd064e44d">WinBioEnumDatabases</a>



<a href="https://msdn.microsoft.com/bd5fd36a-ed90-4dd0-8a84-0412544493dd">WinBioEnumEnrollments</a>



<a href="https://msdn.microsoft.com/2424eae8-4fc6-43f4-97a1-3340870396cc">WinBioEnumServiceProviders</a>
 

 

