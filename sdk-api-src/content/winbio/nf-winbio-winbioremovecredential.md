---
UID: NF:winbio.WinBioRemoveCredential
title: WinBioRemoveCredential function
author: windows-driver-content
description: Deletes a biometric logon credential for a specified user. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbioremovecredential.htm
old-project: SecBioMet
ms.assetid: 56a5d510-f2cb-457b-884a-ad08ea21ce01
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: WINBIO_CREDENTIAL_ALL, WINBIO_CREDENTIAL_PASSWORD, WinBioRemoveCredential, WinBioRemoveCredential function [Windows Biometric Framework API], secbiomet.winbioremovecredential, winbio/WinBioRemoveCredential
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	WinBioRemoveCredential
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioRemoveCredential function


## -description


Deletes a biometric logon credential for a specified user. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param Identity [in]

A  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the SID of the user account for which the logon credential will be removed.


### -param Type [in]

A <a href="https://msdn.microsoft.com/7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3">WINBIO_CREDENTIAL_TYPE</a> value that specifies the credential type. This can be one of the following values:

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
The password-based credential will be deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="WINBIO_CREDENTIAL_ALL"></a><a id="winbio_credential_all"></a><dl>
<dt><b>WINBIO_CREDENTIAL_ALL</b></dt>
</dl>
</td>
<td width="60%">
All logon credentials for the user will be deleted.

</td>
</tr>
</table>
 


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
<dt><b><b>E_ACCESSDENIED</b></b></dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to delete the credential.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_CRED_PROV_NO_CREDENTIAL</b></b></dt>
</dl>
</td>
<td width="60%">
The specified identity does not exist or does not have any related records in the credential store.

</td>
</tr>
</table>
 




## -remarks



Users who do not have elevated privileges can delete only their own credentials. Elevated users can remove credentials for any user account. Deleting a credential does not affect any biometric enrollments for that user. Deleting a biometric credential does not prevent the user from logging on by using a password. Only medium and higher  integrity processes can delete credentials. If a lower integrity process attempts to delete credentials, the function returns E_ACCESSDENIED.


#### Examples

The following function shows how to call <b>WinBioRemoveCredential</b> to remove credentials for a specific user. The helper function  GetCurrentUserIdentity is also included. Link to the Winbio.lib static library and include the following header files:

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
<pre>HRESULT RemoveCredential()
{
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity;

    // Find the identity of the user.
    wprintf_s(L"\n Finding user identity.\n");
    hr = GetCurrentUserIdentity( &amp;identity );
    if (FAILED(hr))
    {
        wprintf(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Remove the user credentials.
    hr = WinBioRemoveCredential(identity, WINBIO_CREDENTIAL_PASSWORD);
    if (FAILED(hr)) 
    {
        wprintf(L"\n WinBioRemoveCredential failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    wprintf_s(L"\n User credentials successfully removed.\n");

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
    Identity-&gt;Type = WINBIO_ID_TYPE_NULL;

    // Open the access token associated with the
    // current process
    if (!OpenProcessToken(
            GetCurrentProcess(),            // Process handle
            TOKEN_READ,                     // Read access only
            &amp;tokenHandle))                  // Access token handle
    {
        DWORD win32Status = GetLastError();
        wprintf_s(L"Cannot open token handle: %d\n", win32Status);
        hr = HRESULT_FROM_WIN32(win32Status);
        goto e_Exit;
    }

    // Zero the tokenInfoBuffer structure.
    ZeroMemory(&amp;tokenInfoBuffer, sizeof(tokenInfoBuffer));

    // Retrieve information about the access token. In this case,
    // retrieve a SID.
    if (!GetTokenInformation(
            tokenHandle,                    // Access token handle
            TokenUser,                      // User for the token
            &amp;tokenInfoBuffer.tokenUser,     // Buffer to fill
            sizeof(tokenInfoBuffer),        // Size of the buffer
            &amp;bytesReturned))                // Size needed
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
        Identity-&gt;Value.AccountSid.Data,
        tokenInfoBuffer.tokenUser.User.Sid
        );

    // Specify the size of the SID and assign WINBIO_ID_TYPE_SID
    // to the type member of the WINBIO_IDENTITY structure.
    Identity-&gt;Value.AccountSid.Size = GetLengthSid(tokenInfoBuffer.tokenUser.User.Sid);
    Identity-&gt;Type = WINBIO_ID_TYPE_SID;

e_Exit:

    if (tokenHandle != NULL)
    {
        CloseHandle(tokenHandle);
    }

    return hr;
}

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3c3f3bed-531a-4962-8eb3-bebe16bed3a8">WinBioRemoveAllCredentials</a>



<a href="https://msdn.microsoft.com/2aee0929-2340-4901-a5d2-f1cd4395624a">WinBioRemoveAllDomainCredentials</a>



<a href="https://msdn.microsoft.com/c35dd874-c545-418a-b08c-82f9e13e93fb">WinBioSetCredential</a>
 

 

