---
UID: NF:winbio.WinBioGetCredentialState
title: WinBioGetCredentialState function (winbio.h)
description: Retrieves a value that specifies whether credentials have been set for the specified user. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
helpviewer_keywords: ["WINBIO_CREDENTIAL_NOT_SET","WINBIO_CREDENTIAL_PASSWORD","WINBIO_CREDENTIAL_SET","WinBioGetCredentialState","WinBioGetCredentialState function [Windows Biometric Framework API]","secbiomet.winbiogetcredentialstate","winbio/WinBioGetCredentialState"]
old-location: secbiomet\winbiogetcredentialstate.htm
tech.root: SecBioMet
ms.assetid: 738b7efb-c796-4f64-95e3-feaaa50ac673
ms.date: 12/05/2018
ms.keywords: WINBIO_CREDENTIAL_NOT_SET, WINBIO_CREDENTIAL_PASSWORD, WINBIO_CREDENTIAL_SET, WinBioGetCredentialState, WinBioGetCredentialState function [Windows Biometric Framework API], secbiomet.winbiogetcredentialstate, winbio/WinBioGetCredentialState
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
 - WinBioGetCredentialState
 - winbio/WinBioGetCredentialState
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
 - WinBioGetCredentialState
---

# WinBioGetCredentialState function


## -description

Retrieves a value that specifies whether credentials have been set for the specified user. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.

## -parameters

### -param Identity [in]

A  <a href="/windows/desktop/SecBioMet/winbio-identity">WINBIO_IDENTITY</a> structure that contains the SID of the user account for which the credential is being queried.

### -param Type [in]

A <a href="/windows/desktop/SecBioMet/winbio-credential-type">WINBIO_CREDENTIAL_TYPE</a> value that specifies the credential type. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_CREDENTIAL_PASSWORD"></a><a id="winbio_credential_password"></a><dl>
<dt><b>WINBIO_CREDENTIAL_PASSWORD</b></dt>
</dl>
</td>
<td width="60%">
The password-based credential is checked.

</td>
</tr>
</table>

### -param CredentialState [out]

Pointer to a <a href="/windows/desktop/SecBioMet/winbio-credential-state">WINBIO_CREDENTIAL_STATE</a> enumeration value that specifies whether user credentials have been set. This can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WINBIO_CREDENTIAL_NOT_SET"></a><a id="winbio_credential_not_set"></a><dl>
<dt><b>WINBIO_CREDENTIAL_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
A credential has not been specified.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_CREDENTIAL_SET"></a><a id="winbio_credential_set"></a><dl>
<dt><b>WINBIO_CREDENTIAL_SET</b></dt>
</dl>
</td>
<td width="60%">
A credential has been specified.

</td>
</tr>
</table>

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
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to retrieve the  credential state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_UNKNOWN_ID</b></b></dt>
</dl>
</td>
<td width="60%">
The specified identity does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_CRED_PROV_DISABLED</b></b></dt>
</dl>
</td>
<td width="60%">
Current administrative policy prohibits use of the credential provider.

</td>
</tr>
</table>

## -remarks

The <b>WinBioGetCredentialState</b> is typically used to provide feedback about credential state in a user interface. For example, an enrollment application might query credential state before prompting a user for credentials.

Call the <a href="/windows/desktop/api/winbio/nf-winbio-winbiosetcredential">WinBioSetCredential</a> function to associate credentials with a user.

Users who do not have elevated privileges can retrieve information about only their own credentials. Elevated users can retrieve information for any credential.


#### Examples

The following function calls <b>WinBioGetCredentialState</b> to retrieve
the credential state for a user. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT GetCredentialState()
{
    // Declare variables.
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity;
    WINBIO_CREDENTIAL_STATE credState;

    // Find the identity of the user.
    wprintf_s(L"\n Finding user identity.\n");
    hr = GetCurrentUserIdentity( &identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        return hr;
    }

    // Find the credential state for the user.
    wprintf_s(L"\n Calling WinBioGetCredentialState.\n");
    hr = WinBioGetCredentialState(
             identity,                      // User GUID or SID
             WINBIO_CREDENTIAL_PASSWORD,    // Credential type
             &credState                     // [out] Credential state
             );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioGetCredentialState failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Print the credential state.
    switch(credState)
    {
        case WINBIO_CREDENTIAL_SET:
            wprintf_s(L"\n Credential set.\n");
            break;
        case WINBIO_CREDENTIAL_NOT_SET:
            wprintf_s(L"\n Credential NOT set.\n");
            break;
        default:
            wprintf_s(L"\n ERROR: Invalid credential state.\n");
            hr = E_FAIL;
    }

e_Exit:

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;

}

//------------------------------------------------------------------------
// The following function retrieves the identity of the current user.
// This is a helper function and is not part of the Windows Biometric
// Framework API.
//
HRESULT GetCurrentUserIdentity(__inout PWINBIO_IDENTITY Identity)
{
    // Declare variables.
    HRESULT hr = S_OK;
    HANDLE tokenHandle = NULL;
    DWORD bytesReturned = 0;
    struct{
        TOKEN_USER tokenUser;
        BYTE buffer[SECURITY_MAX_SID_SIZE];
    } tokenInfoBuffer;

    // Zero the input identity and specify the type.
    ZeroMemory( Identity, sizeof(WINBIO_IDENTITY));
    Identity->Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &bytesReturned))                // Size needed
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot query token information: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Copy the SID from the tokenInfoBuffer structure to the
    // WINBIO_IDENTITY structure. 
    CopySid(
        SECURITY_MAX_SID_SIZE,
        Identity->Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity->Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity->Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}


```

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbiosetcredential">WinBioSetCredential</a>