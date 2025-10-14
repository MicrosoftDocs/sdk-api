---
UID: NF:winbio.WinBioEnumEnrollments
title: WinBioEnumEnrollments function (winbio.h)
description: Retrieves the biometric sub-factors enrolled for a specified identity and biometric unit. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WinBioEnumEnrollments","WinBioEnumEnrollments function [Windows Biometric Framework API]","secbiomet.winbioenumenrollments","winbio/WinBioEnumEnrollments"]
old-location: secbiomet\winbioenumenrollments.htm
tech.root: SecBioMet
ms.assetid: bd5fd36a-ed90-4dd0-8a84-0412544493dd
ms.date: 12/05/2018
ms.keywords: WinBioEnumEnrollments, WinBioEnumEnrollments function [Windows Biometric Framework API], secbiomet.winbioenumenrollments, winbio/WinBioEnumEnrollments
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
 - WinBioEnumEnrollments
 - winbio/WinBioEnumEnrollments
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
 - WinBioEnumEnrollments
---

# WinBioEnumEnrollments function


## -description

Retrieves the biometric sub-factors enrolled for a specified identity and biometric unit. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

### -param UnitId [in]

A <b>WINBIO_UNIT_ID</b> value that specifies the biometric unit.

### -param Identity [in]

Pointer to a  <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that contains the GUID or SID of the template from which the sub-factors are to be retrieved.

### -param SubFactorArray

Address of a variable that receives a pointer to an array of sub-factors. If the function does not succeed, the pointer is set to <b>NULL</b>. If the function succeeds, you must pass the pointer to <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release memory allocated internally for the array.

### -param SubFactorCount [out, optional]

Pointer to a value that specifies the number of elements in the array pointed to by the <i>SubFactorArray</i> parameter. If the function does not succeed, this value is set to zero.

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>UnitId</i> parameter cannot be zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>Identity</i>,  <i>SubFactorArray</i>, and  <i>SubFactorCount</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_ENROLLMENT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed because the biometric unit specified by the <i>UnitId</i> parameter is currently being used for an enrollment transaction.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_UNKNOWN_ID</b></dt>
</dl>
</td>
<td width="60%">
The GUID or SID specified by the <i>Identity</i> parameter cannot be found.

</td>
</tr>
</table>

## -remarks

The <b>WinBioEnumEnrollments</b> function is supplied primarily so that the applications can provide user feedback. For example, your application can call this function to tell the user which fingerprints are already enrolled on a specific fingerprint reader.

After you are finished using the structures returned to the <i>SubFactorArray</i> parameter, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory allocated internally for the array.

To use <b>WinBioEnumEnrollments</b> synchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered.

To use <b>WinBioEnumEnrollments</b> asynchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>. The framework allocates a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. If the operation is successful, the framework returns <b>WINBIO_IDENTITY</b> and <b>WINBIO_BIOMETRIC_SUBTYPE</b> information in a nested <b>EnumEnrollments</b> structure. If the operation is unsuccessful, the framework returns error information. The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.


#### Examples

The following function calls <b>WinBioEnumEnrollments</b> to enumerate the 
biometric sub-factors enrolled for a template.  Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT EnumEnrollments( )
{
    // Declare variables.
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    PWINBIO_BIOMETRIC_SUBTYPE subFactorArray = NULL;
    WINBIO_BIOMETRIC_SUBTYPE SubFactor = 0;
    SIZE_T subFactorCount = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_BIOMETRIC_SUBTYPE subFactor = WINBIO_SUBTYPE_NO_INFORMATION;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the biometric sensor and retrieve a WINBIO_IDENTITY object.
    wprintf_s(L"\n Calling WinBioIdentify - Swipe finger on sensor...\n");
    hr = WinBioIdentify( 
            sessionHandle,              // Session handle
            &unitId,                    // Biometric unit ID
            &identity,                  // User SID
            &subFactor,                 // Finger sub factor
            &rejectDetail               // Rejection information
            );
    wprintf_s(L"\n Swipe processed - Unit ID: %d\n", unitId);
    if (FAILED(hr))
    {
        if (hr == WINBIO_E_UNKNOWN_ID)
        {
            wprintf_s(L"\n Unknown identity.\n");
        }
        else if (hr == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture; reason: %d\n", rejectDetail);
        }
        else
        {
            wprintf_s(L"\n WinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }

    // Retrieve the biometric sub-factors for the template.
    hr = WinBioEnumEnrollments( 
            sessionHandle,              // Session handle
            unitId,                     // Biometric unit ID
            &identity,                  // Template ID
            &subFactorArray,            // Subfactors
            &subFactorCount             // Count of subfactors
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnumEnrollments failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Print the sub-factor(s) to the console.
    wprintf_s(L"\n Enrollments for this user on Unit ID %d:", unitId);
    for (SIZE_T index = 0; index < subFactorCount; ++index)
    {
        SubFactor = subFactorArray[index];
        switch (SubFactor)
        {
            case WINBIO_ANSI_381_POS_RH_THUMB:
                wprintf_s(L"\n   RH thumb\n");
                break;
            case WINBIO_ANSI_381_POS_RH_INDEX_FINGER:
                wprintf_s(L"\n   RH index finger\n");
                break;
            case WINBIO_ANSI_381_POS_RH_MIDDLE_FINGER:
                wprintf_s(L"\n   RH middle finger\n");
                break;
            case WINBIO_ANSI_381_POS_RH_RING_FINGER:
                wprintf_s(L"\n   RH ring finger\n");
                break;
            case WINBIO_ANSI_381_POS_RH_LITTLE_FINGER:
                wprintf_s(L"\n   RH little finger\n");
                break;
            case WINBIO_ANSI_381_POS_LH_THUMB:
                wprintf_s(L"\n   LH thumb\n");
                break;
            case WINBIO_ANSI_381_POS_LH_INDEX_FINGER:
                wprintf_s(L"\n   LH index finger\n");
                break;
            case WINBIO_ANSI_381_POS_LH_MIDDLE_FINGER:
                wprintf_s(L"\n   LH middle finger\n");
                break;
            case WINBIO_ANSI_381_POS_LH_RING_FINGER:
                wprintf_s(L"\n   LH ring finger\n");
                break;
            case WINBIO_ANSI_381_POS_LH_LITTLE_FINGER:
                wprintf_s(L"\n   LH little finger\n");
                break;
            default:
                wprintf_s(L"\n   The sub-factor is not correct\n");
                break;
        }
 
    }

e_Exit:
    if (subFactorArray!= NULL)
    {
        WinBioFree(subFactorArray);
        subFactorArray = NULL;
    }

    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}


```

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumbiometricunits">WinBioEnumBiometricUnits</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumdatabases">WinBioEnumDatabases</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioenumserviceproviders">WinBioEnumServiceProviders</a>