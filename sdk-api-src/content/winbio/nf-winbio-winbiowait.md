---
UID: NF:winbio.WinBioWait
title: WinBioWait function
author: windows-sdk-content
description: Blocks caller execution until all pending biometric operations for a session have been completed or canceled. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbiowait.htm
old-project: secbiomet
ms.assetid: 3cf8b02b-5009-4244-b954-e82d47ed4735
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: WinBioWait, WinBioWait function [Windows Biometric Framework API], secbiomet.winbiowait, winbio/WinBioWait
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
 - WinBioWait
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioWait function


## -description


Blocks caller execution until all pending biometric operations for a session have been completed or canceled. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="https://msdn.microsoft.com/e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>.


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
<dt><b><b>E_HANDLE</b></b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
</table>
 




## -remarks



<b>WinBioWait</b> blocks the caller's thread regardless of whether you pass a synchronous or an asynchronous session handle to the <i>SessionHandle</i> parameter.

Unlike all other functions that can be called by using an asynchronous session handle, the framework does not create a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure for the <b>WinBioWait</b> function.

Do not call <b>WinBioWait</b> from the context of a callback routine or from any function that can be called indirectly from a callback routine. Doing so will cause a permanent deadlock.

Do not call <b>WinBioWait</b> from a window procedure. Doing so will cause the user interface to freeze until the event notification arrives.

If you call <b>WinBioWait</b> from an asynchronous session that generates window messages, there is no guarantee of the order in which the  window message and the wake-from-wait message will arrive. We recommend that you not write any code that depends on the order of these events.


#### Examples

The following code example  shows how to call the <b>WinBioWait</b> function to block execution and wait for an asynchronous thread to finish processing. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT CaptureSampleWithCallback(BOOL bCancel)
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_RAW,            // Raw access
            NULL,                       // Array of biometric unit IDs
            0,                          // Count of biometric unit IDs
            WINBIO_DB_DEFAULT,          // Default database
            &sessionHandle              // [out] Session handle
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Capture a biometric sample asynchronously.
    wprintf_s(L"\n Calling WinBioCaptureSampleWithCallback ");
    hr = WinBioCaptureSampleWithCallback(
            sessionHandle,                  // Open session handle
            WINBIO_NO_PURPOSE_AVAILABLE,    // Intended use of the sample
            WINBIO_DATA_FLAG_RAW,           // Sample format
            CaptureSampleCallback,          // Callback function
            NULL                            // Optional context
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioCaptureSampleWithCallback failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Swipe the sensor ...\n");

    // Cancel the identification if the bCancel flag is set.
    if (bCancel)
    {
        wprintf_s(L"\n Starting CANCEL timer...");
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

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for WinBioCaptureSampleWithCallback.
// The function filters the response from the biometric subsystem and 
// writes a result to the console window.
//
VOID CALLBACK CaptureSampleCallback(
    __in_opt PVOID CaptureCallbackContext,
    __in HRESULT OperationStatus,
    __in WINBIO_UNIT_ID UnitId,
    __in_bcount(SampleSize) PWINBIO_BIR Sample,
    __in SIZE_T SampleSize,
    __in WINBIO_REJECT_DETAIL RejectDetail
    )
{
    UNREFERENCED_PARAMETER(CaptureCallbackContext);

    wprintf_s(L"\n CaptureSampleCallback executing");
    wprintf_s(L"\n Swipe processed - Unit ID: %d", UnitId);

    if (FAILED(OperationStatus))
    {
        if (OperationStatus == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture; reason: %d\n", RejectDetail);
         }
        else
        {
            wprintf_s(L"\n WinBioCaptureSampleWithCallback failed. ");
            wprintf_s(L" OperationStatus = 0x%x\n", OperationStatus);
        }
        goto e_Exit;
    }

    wprintf_s(L"\n Captured %d bytes.\n", SampleSize);

e_Exit:

    if (Sample != NULL)
    {
        WinBioFree(Sample);
        Sample = NULL;
    }
}


```





## -see-also




<a href="https://msdn.microsoft.com/a99296c8-89da-4b2c-9a1b-fc10700ad48d">WinBioCaptureSampleWithCallback</a>



<a href="https://msdn.microsoft.com/809e7d2f-6b41-4afc-86c2-43b6611d6e48">WinBioEnrollCaptureWithCallback</a>



<a href="https://msdn.microsoft.com/df96b444-4a94-4d12-9d7a-2543d96f89ea">WinBioIdentifyWithCallback</a>



<a href="https://msdn.microsoft.com/d94db51b-67da-477a-82e6-c92da756f017">WinBioLocateSensorWithCallback</a>



<a href="https://msdn.microsoft.com/4ea03163-062a-4abf-837a-b12b03ada375">WinBioVerifyWithCallback</a>
 

 

