---
UID: NC:winbio.PWINBIO_ENROLL_CAPTURE_CALLBACK
title: PWINBIO_ENROLL_CAPTURE_CALLBACK
author: windows-sdk-content
description: Called by the Windows Biometric Framework to return results from the asynchronous WinBioEnrollCaptureWithCallback function.
old-location: secbiomet\pwinbio_enroll_capture_callback.htm
old-project: secbiomet
ms.assetid: B43C8A68-4D39-4275-891C-2DFE97DC4D64
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: PWINBIO_ENROLL_CAPTURE_CALLBACK, PWINBIO_ENROLL_CAPTURE_CALLBACK function, PWINBIO_ENROLL_CAPTURE_CALLBACK function pointer [Windows Biometric Framework API], secbiomet.pwinbio_enroll_capture_callback, winbio/PWINBIO_ENROLL_CAPTURE_CALLBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winbio.h
req.include-header: 
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
req.typenames: WIN32_STREAM_ID, *LPWIN32_STREAM_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio.h
api_name:
 - PWINBIO_ENROLL_CAPTURE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PWINBIO_ENROLL_CAPTURE_CALLBACK callback function


## -description


The <b>PWINBIO_ENROLL_CAPTURE_CALLBACK</b> function is called by the Windows Biometric Framework to return results from the   asynchronous  <a href="https://msdn.microsoft.com/809e7d2f-6b41-4afc-86c2-43b6611d6e48">WinBioEnrollCaptureWithCallback</a> function. The client application must implement this function.


<div class="alert"><b>Important</b>  We recommend that, beginning with Windows 8, you no longer use the <b>PWINBIO_ENROLL_CAPTURE_CALLBACK</b>/<b>WinBioEnrollCaptureWithCallback</b> combination. Instead, do the following:<ul>
<li>Implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function to receive notice when the operation completes.</li>
<li>Call the <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> function. Pass the address of your callback in the <i>CallbackRoutine</i> parameter. Pass  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter. Retrieve an asynchronous session handle.</li>
<li>Use the asynchronous session handle to call <a href="https://msdn.microsoft.com/a50f0c9f-7b9c-4d80-b8fc-8b83bc333578">WinBioEnrollCapture</a>. When the operation finishes, the Windows Biometric Framework will allocate and initialize a  <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure with the results and invoke your callback with a pointer to the results structure.</li>
<li>Call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> from your callback implementation to release the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.</li>
</ul>
</div>
<div> </div>



## -parameters




### -param EnrollCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>EnrollCallback</i> parameter of the <a href="https://msdn.microsoft.com/809e7d2f-6b41-4afc-86c2-43b6611d6e48">WinBioEnrollCaptureWithCallback</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.


### -param OperationStatus [in]

Error code returned by the capture operation.


### -param RejectDetail [in]

Additional information about the failure, if any, to perform the operation. For more information,  see Remarks.


## -returns



Do not return a value from your implementation of this function.




## -remarks



Currently, the Windows Biometric Framework supports only fingerprint readers. Therefore, if an operation fails and returns additional information in a <b>WINBIO_REJECT_DETAIL</b> constant, it will be one of the following values:<ul>
<li>WINBIO_FP_TOO_HIGH</li>
<li>WINBIO_FP_TOO_LOW</li>
<li>WINBIO_FP_TOO_LEFT</li>
<li>WINBIO_FP_TOO_RIGHT</li>
<li>WINBIO_FP_TOO_FAST</li>
<li>WINBIO_FP_TOO_SLOW</li>
<li>WINBIO_FP_POOR_QUALITY</li>
<li>WINBIO_FP_TOO_SKEWED</li>
<li>WINBIO_FP_TOO_SHORT</li>
<li>WINBIO_FP_MERGE_FAILURE</li>
</ul>



#### Examples

The following code example enrolls a fingerprint asynchronously by calling <a href="https://msdn.microsoft.com/809e7d2f-6b41-4afc-86c2-43b6611d6e48">WinBioEnrollCaptureWithCallback</a> and passing a pointer to a custom callback function, EnrollCaptureCallback. Link to the Winbio.lib static library.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//------------------------------------------------------------------------
// EnrollSystemPoolWithCallback.cpp : console application entry point.
//

#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;conio.h&gt;
#include &lt;winbio.h&gt;


//------------------------------------------------------------------------
// Forward declarations.
//
HRESULT EnrollSysPoolWithCallback(
                      BOOL bCancel,
                      BOOL bDiscard,
                      WINBIO_BIOMETRIC_SUBTYPE subFactor);

VOID CALLBACK EnrollCaptureCallback(
                      __in_opt PVOID EnrollCallbackContext,
                      __in HRESULT OperationStatus,
                      __in WINBIO_REJECT_DETAIL RejectDetail);

typedef struct _ENROLL_CALLBACK_CONTEXT {
    WINBIO_SESSION_HANDLE SessionHandle;
    WINBIO_UNIT_ID UnitId;
    WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} ENROLL_CALLBACK_CONTEXT, *PENROLL_CALLBACK_CONTEXT;

//------------------------------------------------------------------------
int wmain()
{
    HRESULT hr = S_OK;

    hr = EnrollSysPoolWithCallback(
                      FALSE, 
                      FALSE, 
                      WINBIO_ANSI_381_POS_RH_INDEX_FINGER);

    return 0;
}

//------------------------------------------------------------------------
// The following function enrolls a user's fingerprint in the system pool.
// The function calls WinBioEnrollCaptureWithCallback and waits for the
// asynchronous enrollment process to be completed or canceled.
//
HRESULT EnrollSysPoolWithCallback(
                      BOOL bCancel,
                      BOOL bDiscard,
                      WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    // Declare variables
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    BOOLEAN isNewTemplate = TRUE;
    ENROLL_CALLBACK_CONTEXT callbackContext = {0};

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
        wprintf_s(L"\n WinBioEnumBiometricUnits failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate the sensor.
    wprintf_s(L"\n Swipe your finger to locate the sensor...\n");
    hr = WinBioLocateSensor( sessionHandle, &amp;unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Begin the enrollment sequence. 
    hr = WinBioEnrollBegin(
            sessionHandle,      // Handle to open biometric session
            subFactor,          // Finger to create template for
            unitId              // Biometric unit ID
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollBegin failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Set up the custom callback context structure.
    callbackContext.SessionHandle = sessionHandle;
    callbackContext.UnitId = unitId;
    callbackContext.SubFactor = subFactor;

    // Call WinBioEnrollCaptureWithCallback. This is an asynchronous
    // method that returns immediately.
    hr = WinBioEnrollCaptureWithCallback(
            sessionHandle,          // Handle to open biometric session
            EnrollCaptureCallback,  // Callback function
            &amp;callbackContext        // Pointer to the custom context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioEnrollCaptureWithCallback failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor with the appropriate finger...\n");

    // Cancel the enrollment if the bCancel flag is set.
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

    // Wait for the asynchronous enrollment process to complete
    // or be canceled.
    hr = WinBioWait( sessionHandle );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioWait failed. hr = 0x%x\n", hr);
    }

    // Discard the enrollment if the bDiscard flag is set.
    // Commit the enrollment if the flag is not set.
    if (bDiscard)
    {
        wprintf_s(L"\n Discarding enrollment...\n");
        hr = WinBioEnrollDiscard( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioLocateSensor failed. ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }
        goto e_Exit;    
    }
    else
    {
        wprintf_s(L"\n Committing enrollment...\n");
        hr = WinBioEnrollCommit( 
                sessionHandle,      // Handle to open biometric session
                &amp;identity,          // WINBIO_IDENTITY object for the user
                &amp;isNewTemplate);    // Is this a new template

        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioEnrollCommit failed. hr = 0x%x\n", hr);
            goto e_Exit;
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

//------------------------------------------------------------------------
// The following function is the callback for the Windows Biometric
// Framework WinBioEnrollCaptureWithCallback() function. 
//
VOID CALLBACK EnrollCaptureCallback(
    __in_opt PVOID EnrollCallbackContext,
    __in HRESULT OperationStatus,
    __in WINBIO_REJECT_DETAIL RejectDetail
    )
{
    // Declare variables.
    HRESULT hr = S_OK; 
    static SIZE_T swipeCount = 1;

    PENROLL_CALLBACK_CONTEXT callbackContext = 
        (PENROLL_CALLBACK_CONTEXT)EnrollCallbackContext;

    wprintf_s(L"\n EnrollCaptureCallback executing\n");
    wprintf_s(L"\n Sample %d captured", swipeCount++);

    // The capture was not acceptable or the enrollment operation
    // failed.
    if (FAILED(OperationStatus))
    {
        if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
            wprintf_s(L"\n Swipe your finger to capture another sample.\n");

            // Try again.
            hr = WinBioEnrollCaptureWithCallback(
                    callbackContext-&gt;SessionHandle, // Open session handle
                    EnrollCaptureCallback,          // Callback function
                    EnrollCallbackContext           // Callback context
                    );
            if (FAILED(hr))
            {
                wprintf_s(L"WinBioEnrollCaptureWithCallback failed.");
                wprintf_s(L"hr = 0x%x\n", hr);
            }
        }
        else
        {
            wprintf_s(L"EnrollCaptureCallback failed.");
            wprintf_s(L"OperationStatus = 0x%x\n", OperationStatus);
        }
        goto e_Exit;
    }

    // The enrollment operation requires more fingerprint swipes.
    // This is normal and depends on your hardware. Typically, at least
    // three swipes are required.
    if (OperationStatus == WINBIO_I_MORE_DATA)
    {
        wprintf_s(L"\n More data required.");
        wprintf_s(L"\n Swipe your finger on the sensor again.");

        hr = WinBioEnrollCaptureWithCallback(
                callbackContext-&gt;SessionHandle,
                EnrollCaptureCallback,
                EnrollCallbackContext
                );
        if (FAILED(hr))
        {
            wprintf_s(L"WinBioEnrollCaptureWithCallback failed. ");
            wprintf_s(L"hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }

    wprintf_s(L"\n Template completed\n");

e_Exit:

    return;
}

</pre>
</td>
</tr>
</table></span></div>


