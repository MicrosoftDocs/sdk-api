---
UID: NF:winbio.WinBioVerifyWithCallback
title: WinBioVerifyWithCallback function
author: windows-sdk-content
description: Asynchronously captures a biometric sample and determines whether the sample corresponds to the specified user identity.
old-location: secbiomet\winbioverifywithcallback.htm
tech.root: SecBioMet
ms.assetid: 4ea03163-062a-4abf-837a-b12b03ada375
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WinBioVerifyWithCallback, WinBioVerifyWithCallback function [Windows Biometric Framework API], secbiomet.winbioverifywithcallback, winbio/WinBioVerifyWithCallback
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
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
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
 - WinBioVerifyWithCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WinBioVerifyWithCallback
: 
---

# WinBioVerifyWithCallback function


## -description


Asynchronously captures a biometric sample and determines whether the sample corresponds to the specified user identity.  The function returns immediately to the caller, performs capture and verification on a separate thread, and calls into an application-defined callback function to update operation status.


<div class="alert"><b>Important</b>  <p class="note">We recommend that, beginning with Windows 8, you no longer use this function to start an asynchronous operation. Instead, do the following:

<ul>
<li>Implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function to receive notice when the operation completes.</li>
<li>Call the <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> function. Pass the address of your callback in the <i>CallbackRoutine</i> parameter. Pass  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter. Retrieve an asynchronous session handle.</li>
<li>Use the asynchronous session handle to call <a href="https://msdn.microsoft.com/7266ca33-d3f9-421f-8265-e23a3ec3a77e">WinBioVerify</a>. When the operation finishes, the Windows Biometric Framework will allocate and initialize a  <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure with the results and invoke your callback with a pointer to the results structure.</li>
<li>Call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> from your callback implementation to release the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.</li>
</ul>
</div>
<div> </div>



## -parameters




### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.


### -param Identity [in]

Pointer to a  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that contains the GUID or SID of the user providing the biometric sample.


### -param SubFactor [in]

A <b>WINBIO_BIOMETRIC_SUBTYPE</b> value that specifies the sub-factor associated with the biometric sample. See the Remarks section for more details.


### -param VerifyCallback [in]

Address of a callback function that will be called by the <b>WinBioVerifyWithCallback</b> function when verification succeeds or fails. You must create the callback.


### -param VerifyCallbackContext [in, optional]

An optional application-defined structure that is returned in the <i>VerifyCallbackContext</i> parameter of the callback function. This structure can contain any data that the custom callback function is designed to handle.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_HANDLE</b></b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>SubFactor</i> argument is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The pointer specified by the <i>Identity</i> and <i>VerifyCallback</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The <i>SubFactor</i> parameter specifies the sub-factor associated with the biometric sample. The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.

<ul>
<li><b>WINBIO_ANSI_381_POS_RH_THUMB</b></li>
<li><b>WINBIO_ANSI_381_POS_RH_INDEX_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_RH_MIDDLE_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_RH_RING_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_RH_LITTLE_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_LH_THUMB</b></li>
<li><b>WINBIO_ANSI_381_POS_LH_INDEX_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_LH_MIDDLE_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_LH_RING_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_LH_LITTLE_FINGER</b></li>
<li><b>WINBIO_ANSI_381_POS_RH_FOUR_FINGERS</b></li>
<li><b>WINBIO_ANSI_381_POS_LH_FOUR_FINGERS</b></li>
</ul>
The callback routine executes in the context of an arbitrary thread in the calling process. The caller is responsible for synchronizing access to any memory that may be shared between the callback and other parts of the application.

The <b>WinBioVerifyWithCallback</b> function returns immediately and passes S_OK to the caller. To determine the status of the capture and verification process, you must examine the <i>OperationStatus</i> parameter in your callback function.

You can call the <a href="https://msdn.microsoft.com/62176608-1545-47d2-b4be-37bb2a4a064b">WinBioCancel</a> function to cancel a pending callback operation. Closing a session also implicitly cancels callbacks for that session.

The callback routine must have the following signature:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID CALLBACK VerifyCallback(
__in_opt PVOID VerifyCallbackContext,
__in HRESULT OperationStatus,
__in WINBIO_UNIT_ID UnitId,
__in BOOLEAN Match,
__in WINBIO_REJECT_DETAIL RejectDetail
);</pre>
</td>
</tr>
</table></span></div>

#### Examples

The following function calls <b>WinBioVerifyWithCallback</b> to asynchronously 
determine whether a biometric sample matches the logged on identity of
the current user. The callback routine, VerifyCallback, and a helper function, GetCurrentUserIdentity, are also included. Link to the Winbio.lib static library and include the following header files:

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
<pre>HRESULT VerifyWithCallback(BOOL bCancel, WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    // Declare variables.
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    WINBIO_IDENTITY identity = {0};

    // Find the identity of the user.
    hr = GetCurrentUserIdentity( &amp;identity );
    if (FAILED(hr))
    {
        wprintf_s(L"\n User identity not found. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_DEFAULT,        // Configuration and access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            NULL,                       // Database ID
            &amp;sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Verify a biometric sample asynchronously.
    wprintf_s(L"\n Calling WinBioVerifyWithCallback.\n");
    hr = WinBioVerifyWithCallback(
            sessionHandle,              // Open session handle
            &amp;identity,                  // User SID or GUID
            subFactor,                  // Sample sub-factor
            VerifyCallback,             // Callback function
            NULL                        // Optional context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioVerifyWithCallback failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor ...\n");

    // Cancel the identification if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...\n");
        Sleep( 7000 );

        wprintf_s(L"\n Calling WinBioCancel\n");
        hr = WinBioCancel( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCancel failed. hr = 0x%x\n", hr);
            goto e_Exit;
        }
    }

    // Wait for the asynchronous identification process to complete 
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

e_Exit:
    if (sessionHandle != NULL)
    {
        WinBioCloseSession(sessionHandle);
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Hit any key to continue...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for WinBioVerifyWithCallback.
// The function filters the response from the biometric subsystem and 
// writes a result to the console window.
// 
VOID CALLBACK VerifyCallback(
  __in_opt PVOID VerifyCallbackContext,
  __in HRESULT OperationStatus,
  __in WINBIO_UNIT_ID UnitId,
  __in BOOLEAN Match,
  __in WINBIO_REJECT_DETAIL RejectDetail
  )
{
    UNREFERENCED_PARAMETER(VerifyCallbackContext);
    UNREFERENCED_PARAMETER(Match);

    wprintf_s(L"\n VerifyCallback executing");
    wprintf_s(L"\n Swipe processed for unit ID %d\n", UnitId);

    // The identity could not be verified.
    if (FAILED(OperationStatus))
    {
        wprintf_s(L"\n Verification failed for the following reason:");
        if (OperationStatus == WINBIO_E_NO_MATCH)
        {
            wprintf_s(L"\n No match.\n");
        }
        else if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture.\n ");
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
        }
        else
        {
            wprintf_s(L"VerifyCallback failed.");
            wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus); 
        }
        goto e_Exit;
    }

    // The user identity was verified.
    wprintf_s(L"\n Fingerprint verified:\n");

e_Exit:
    return;
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




<a href="https://msdn.microsoft.com/62176608-1545-47d2-b4be-37bb2a4a064b">WinBioCancel</a>



<a href="https://msdn.microsoft.com/7266ca33-d3f9-421f-8265-e23a3ec3a77e">WinBioVerify</a>
 

 

