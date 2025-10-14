---
UID: NF:winbio.WinBioLogonIdentifiedUser
title: WinBioLogonIdentifiedUser function (winbio.h)
description: Causes a fast user switch to the account associated with the last successful identification operation performed by the biometric session.
helpviewer_keywords: ["WinBioLogonIdentifiedUser","WinBioLogonIdentifiedUser function [Windows Biometric Framework API]","secbiomet.winbiologonidentifieduser","winbio/WinBioLogonIdentifiedUser"]
old-location: secbiomet\winbiologonidentifieduser.htm
tech.root: SecBioMet
ms.assetid: 0df6da19-e23b-445f-82d9-bd51cda3ae15
ms.date: 12/05/2018
ms.keywords: WinBioLogonIdentifiedUser, WinBioLogonIdentifiedUser function [Windows Biometric Framework API], secbiomet.winbiologonidentifieduser, winbio/WinBioLogonIdentifiedUser
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
 - WinBioLogonIdentifiedUser
 - winbio/WinBioLogonIdentifiedUser
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
 - WinBioLogonIdentifiedUser
---

# WinBioLogonIdentifiedUser function


## -description

The <b>WinBioLogonIdentifiedUser</b> function causes a fast user switch to the account associated with the last successful identification operation performed by the biometric session.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies the biometric session that has recently performed a successful identification operation. Open the session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to switch users or the biometric session is out of date.

</td>
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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The user identified by the <i>SessionHandle</i> parameter is the same as the current user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_LOGON_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user could not be logged on.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_CRED_PROV_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Current administrative policy prohibits use of the credential provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_FAST_USER_SWITCH_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Fast user switching is not enabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_SAS_ENABLED</b></dt>
</dl>
</td>
<td width="60%">
Fast user switching cannot be performed because secure logon (CTRL+ALT+DELETE) is currently enabled.

</td>
</tr>
</table>

## -remarks

The <b>WinBioLogonIdentifiedUser</b> function is typically called by applications that support fast user switching when they identify a user other than the one who is currently logged on.

The fast user switch attempt can leave a logon event in the security log, but the identity is not automatically stored when the credential manager terminates.

The biometric session specified by the <i>SessionHandle</i> parameter controls the target account for the fast user switch event. If that handle has been used recently to perform an identification operation, the resulting identity will be logged in after the fast user switch.

For security reasons, the Windows Biometric Framework requires that the identification operation and the call to <b>WinBioLogonIdentifiedUser</b> happen within a short period of time. After that period, the identification is considered to be out of date and the call to <b>WinBioLogonIdentifiedUser</b> will fail. The default timeout interval is five seconds, but an  administrator can make it as large as 60 seconds.

Calling this function when the target user is the same as the current user returns <b>S_FALSE</b> and the fast user switch attempt is ignored.


#### Examples

The following function calls WinBioLogonIdentifiedUser to log on a
previously identified user. For this function to work correctly, secure logon must not be enabled.   Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT LogonIdentifiedUser()
{
    // Declare variables.
    HRESULT hr;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID  UnitId;
    WINBIO_IDENTITY Identity;
    WINBIO_BIOMETRIC_SUBTYPE SubFactor;
    WINBIO_REJECT_DETAIL RejectDetail;
    BOOL    bContinue = TRUE;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            WINBIO_DB_DEFAULT,                       // Database ID
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the biometric sensor and retrieve a WINBIO_IDENTITY object.
    // You must swipe your finger on the sensor.
    wprintf_s(L"\n Calling WinBioIdentify - Swipe finger on sensor...\n");
    while(bContinue)
    {
        hr = WinBioIdentify(
                sessionHandle,          // Session handle    
                &UnitId,                // Biometric unit ID
                &Identity,              // User SID or GUID
                &SubFactor,             // Finger sub factor
                &RejectDetail           // rejection information
                );

        switch(hr)
        {
        case S_OK:
            bContinue = FALSE;
            break;
        default:
            wprintf_s(L"\n WinBioIdentify failed. hr = 0x%x\n", hr);
            break;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Switch to the target after receiving a good identity.
        hr = WinBioLogonIdentifiedUser(sessionHandle);

        switch(hr)
        {
        case S_FALSE:
            printf("\n Target is the logged on user. No action taken.\n");
            break;
        case S_OK:
            printf("\n Fast user switch initiated.\n");
            break;
        default:
            wprintf_s(L"\n WinBioLogonIdentifiedUser failed. hr = 0x%x\n", hr);
            break;
        }
    }

e_Exit:

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

<a href="/windows/desktop/api/winbio/nf-winbio-winbioidentify">WinBioIdentify</a>



<a href="/windows/desktop/api/winbio/nf-winbio-winbioidentifywithcallback">WinBioIdentifyWithCallback</a>