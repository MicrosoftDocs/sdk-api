---
UID: NF:winbio.WinBioCaptureSampleWithCallback
title: WinBioCaptureSampleWithCallback function (winbio.h)
description: Captures a biometric sample asynchronously and returns the raw or processed data in a biometric information record (BIR).
helpviewer_keywords: ["WINBIO_DATA_FLAG_INTEGRITY","WINBIO_DATA_FLAG_INTERMEDIATE","WINBIO_DATA_FLAG_PRIVACY","WINBIO_DATA_FLAG_PROCESSED","WINBIO_DATA_FLAG_RAW","WINBIO_DATA_FLAG_SIGNED","WinBioCaptureSampleWithCallback","WinBioCaptureSampleWithCallback function [Windows Biometric Framework API]","secbiomet.winbiocapturesamplewithcallback","winbio/WinBioCaptureSampleWithCallback"]
old-location: secbiomet\winbiocapturesamplewithcallback.htm
tech.root: SecBioMet
ms.assetid: a99296c8-89da-4b2c-9a1b-fc10700ad48d
ms.date: 11/19/2020
ms.keywords: WINBIO_DATA_FLAG_INTEGRITY, WINBIO_DATA_FLAG_INTERMEDIATE, WINBIO_DATA_FLAG_PRIVACY, WINBIO_DATA_FLAG_PROCESSED, WINBIO_DATA_FLAG_RAW, WINBIO_DATA_FLAG_SIGNED, WinBioCaptureSampleWithCallback, WinBioCaptureSampleWithCallback function [Windows Biometric Framework API], secbiomet.winbiocapturesamplewithcallback, winbio/WinBioCaptureSampleWithCallback
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
 - WinBioCaptureSampleWithCallback
 - winbio/WinBioCaptureSampleWithCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - WinBioExt.dll
 - Ext-MS-Win-BioMetrics-WinBio-l1-2-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-L1-3-0.dll
api_name:
 - WinBioCaptureSampleWithCallback
---

# WinBioCaptureSampleWithCallback function


## -description

Captures a biometric sample asynchronously and returns the raw or processed data in a biometric information record (BIR). The function returns immediately to the caller, captures the sample on a separate thread, and calls into an application-defined callback function to update operation status.


<div class="alert"><b>Important</b>  <p class="note">We recommend that, beginning with Windows 8, you no longer use this function to start an asynchronous operation. Instead, do the following:

<ul>
<li>Implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function to receive notice when the operation completes.</li>
<li>Call the <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> function. Pass the address of your callback in the <i>CallbackRoutine</i> parameter. Pass  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter. Retrieve an asynchronous session handle.</li>
<li>Use the asynchronous session handle to call <a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>. When the operation finishes, the Windows Biometric Framework will allocate and initialize a  <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure with the results and invoke your callback with a pointer to the results structure.</li>
<li>Call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> from your callback implementation to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.</li>
</ul>
</div>
<div> </div>

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.

### -param Purpose [in]

A <b>WINBIO_BIR_PURPOSE</b> bitmask that specifies the intended use of the sample.  This can be a bitwise <b>OR</b> of the following values:

<ul>
<li><b>WINBIO_PURPOSE_VERIFY</b></li>
<li><b>WINBIO_PURPOSE_IDENTIFY</b></li>
<li><b>WINBIO_PURPOSE_ENROLL</b></li>
<li><b>WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION</b></li>
<li><b>WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION</b></li>
</ul>

### -param Flags [in]

A value that specifies the type of processing to be applied to the captured sample. This can be a bitwise <b>OR</b> of the following security and processing level flags:

* **WINBIO_DATA_FLAG_PRIVACY**

Encrypt the sample.

* **WINBIO_DATA_FLAG_INTEGRITY**

Sign the sample or protect it by using a message authentication code (MAC).

* **WINBIO_DATA_FLAG_SIGNED**

If this flag and the WINBIO_DATA_FLAG_INTEGRITYflag are set, sign the sample. If this flag is not set but the WINBIO_DATA_FLAG_INTEGRITY flag is set, compute a MAC.

* **WINBIO_DATA_FLAG_RAW**

Return the sample exactly as it was captured by the sensor.

* **WINBIO_DATA_FLAG_INTERMEDIATE**

Return the sample after it has been cleaned and filtered.

* **WINBIO_DATA_FLAG_PROCESSED**

Return the sample after it is ready to be used for the purpose specified by the <mark>Purpose</mark> parameter.

### -param CaptureCallback [in]

Address of a callback function that will be called by the <b>WinBioCaptureSampleWithCallback</b> function when the capture operation succeeds or fails. You must create the callback.

### -param CaptureCallbackContext [in, optional]

Address of an application-defined data structure that is passed to the callback function in its <i>CaptureCallbackContext</i> parameter. This structure can contain any data that the custom callback function is designed to handle.

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
The caller does not have permission to capture raw samples, or the session was not opened by using the <b>WINBIO_FLAG_RAW</b> flag.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The biometric unit does not support the requested operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>UnitId</i>, <i>Sample</i>, <i>SampleSize</i>, and <i>RejectDetail</i> pointers cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_ENROLLMENT_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed because the biometric unit is currently being used for an enrollment transaction (system pool only).

</td>
</tr>
</table>

## -remarks

The <b>WinBioCaptureSampleWithCallback</b> function captures samples asynchronously. To call this function successfully, the session handle must have been opened by specifying <b>WINBIO_FLAG_RAW</b>. Only the Administrators and Local System accounts have the necessary privileges.

Valid combinations of the <i>Purpose</i> and <i>Flags</i> parameters depend on the capabilities of the biometric unit being used. Consult the vendor sensor  documentation to determine what combinations are supported and how they affect the captured data.

Callers are responsible for releasing the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure returned by the <i>Sample</i> parameter.

The callback routine must have the following signature:


```cpp
VOID CALLBACK CaptureCallback(
__in_opt PVOID CaptureCallbackContext,
__in HRESULT OperationStatus,
__in WINBIO_UNIT_ID UnitId,
__in_bcount(SampleSize) PWINBIO_BIR Sample,
__in SIZE_T SampleSize,
__in WINBIO_REJECT_DETAIL RejectDetail
);

```



#### Examples

The following code example captures a sample asynchronously by calling <b>WinBioCaptureSampleWithCallback</b> and passing a pointer to a custom callback function. The callback function, CaptureSampleCallback, is also shown. Link to the Winbio.lib static library and include the following header files:

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

    // Cancel the capture process if the bCancel flag is set.
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

    // Wait for the asynchronous capture process to complete 
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

<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesample">WinBioCaptureSample</a>