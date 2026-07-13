---
UID: NF:winbio.WinBioUnlockUnit
title: WinBioUnlockUnit function (winbio.h)
description: Releases the session lock on the specified biometric unit.
helpviewer_keywords: ["WinBioUnlockUnit","WinBioUnlockUnit function [Windows Biometric Framework API]","secbiomet.winbiounlockunit","winbio/WinBioUnlockUnit"]
old-location: secbiomet\winbiounlockunit.htm
tech.root: SecBioMet
ms.assetid: 689adf39-da62-4e83-94e9-e2daa7bd4753
ms.date: 12/05/2018
ms.keywords: WinBioUnlockUnit, WinBioUnlockUnit function [Windows Biometric Framework API], secbiomet.winbiounlockunit, winbio/WinBioUnlockUnit
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
 - WinBioUnlockUnit
 - winbio/WinBioUnlockUnit
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
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - winbioext.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioUnlockUnit
---

# WinBioUnlockUnit function


## -description

Releases the session lock on the specified biometric unit.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

### -param UnitId [in]

A <b>WINBIO_UNIT_ID</b> value that specifies the biometric unit to unlock.

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
The <i>UnitId</i> parameter cannot contain zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_LOCK_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
The biometric unit specified by the <i>UnitId</i> parameter is not currently locked by the session.

</td>
</tr>
</table>

## -remarks

Calling <b>WinBioUnlockUnit</b> automatically releases any locks held by the session. This function will fail if the biometric unit specified by the <i>UnitId</i> has not been previously locked by calling the <a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a> function.

To use <b>WinBioUnlockUnit</b> synchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered.

To use <b>WinBioUnlockUnit</b> asynchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>. The framework allocates a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.


#### Examples

The following function calls <a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a> to lock the biometric
unit before calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioidentify">WinBioIdentify</a> to identify the user.  It calls <b>WinBioUnlockUnit</b> to unlock the biometric union before closing the open session. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT LockUnlock( )
{
    // Declare variables.
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_BIOMETRIC_SUBTYPE subFactor = WINBIO_SUBTYPE_NO_INFORMATION;
    BOOL lockAcquired = FALSE;

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
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Lock the session. The Biometric unit ID (1) is hard coded in
    // this example.
    hr = WinBioLockUnit( sessionHandle, 1 );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLockUnit failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Biometric unit #1 is locked.\n");
    lockAcquired = TRUE;


    // Locate the biometric sensor and retrieve a WINBIO_IDENTITY object.
    // You must swipe your finger on the sensor.
    wprintf_s(L"\n Calling WinBioIdentify - Swipe finger on sensor...\n");
    hr = WinBioIdentify( 
            sessionHandle, 
            &unitId, 
            &identity, 
            &subFactor, 
            &rejectDetail
            );
    wprintf_s(L"\n Swipe processed - Unit ID: %d\n", unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioIdentify failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }


e_Exit:

    // Unlock the biometric unit if it is locked.
    if (lockAcquired == TRUE)
    {
        hr = WinBioUnlockUnit( sessionHandle, 1 );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioUnlockUnit failed. hr = 0x%x\n", hr);
        }
        wprintf_s(L"\n Biometric unit #1 is unlocked.\n");
        lockAcquired = FALSE;
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

<a href="/windows/desktop/api/winbio/nf-winbio-winbiolockunit">WinBioLockUnit</a>