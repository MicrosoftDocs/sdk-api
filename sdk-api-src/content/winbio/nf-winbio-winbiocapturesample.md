---
UID: NF:winbio.WinBioCaptureSample
title: WinBioCaptureSample function (winbio.h)
description: Captures a biometric sample and fills a biometric information record (BIR) with the raw or processed data.
helpviewer_keywords: ["WINBIO_DATA_FLAG_INTEGRITY","WINBIO_DATA_FLAG_INTERMEDIATE","WINBIO_DATA_FLAG_PRIVACY","WINBIO_DATA_FLAG_PROCESSED","WINBIO_DATA_FLAG_RAW","WINBIO_DATA_FLAG_SIGNED","WinBioCaptureSample","WinBioCaptureSample function [Windows Biometric Framework API]","secbiomet.winbiocapturesample","winbio/WinBioCaptureSample"]
old-location: secbiomet\winbiocapturesample.htm
tech.root: SecBioMet
ms.assetid: 365dcefb-3382-4b62-b47d-919e2d3f56f1
ms.date: 11/17/2020
ms.keywords: WINBIO_DATA_FLAG_INTEGRITY, WINBIO_DATA_FLAG_INTERMEDIATE, WINBIO_DATA_FLAG_PRIVACY, WINBIO_DATA_FLAG_PROCESSED, WINBIO_DATA_FLAG_RAW, WINBIO_DATA_FLAG_SIGNED, WinBioCaptureSample, WinBioCaptureSample function [Windows Biometric Framework API], secbiomet.winbiocapturesample, winbio/WinBioCaptureSample
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
 - WinBioCaptureSample
 - winbio/WinBioCaptureSample
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
 - WinBioCaptureSample
---

# WinBioCaptureSample function


## -description

Captures a biometric sample and fills a biometric information record (BIR) with the raw or processed data.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>.

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

Sign the sample or protect it by using a message authentication code (MAC)
    
* **WINBIO_DATA_FLAG_SIGNED**
      
If this flag and the WINBIO_DATA_FLAG_INTEGRITY flag are set, sign the sample. If this flag is not set but the WINBIO_DATA_FLAG_INTEGRITY flag is set, compute a MAC.
   
* **WINBIO_DATA_FLAG_RAW**

Return the sample exactly as it was captured by the sensor.
   
* **WINBIO_DATA_FLAG_INTERMEDIATE**

Return the sample after it has been cleaned and filtered.
   
* **WINBIO_DATA_FLAG_PROCESSED**
   
Return the sample after it is ready to be used for the purpose specified by the Purpose parameter.


### -param UnitId [out, optional]

A pointer to a <b>WINBIO_UNIT_ID</b> value that contains the ID of  the biometric unit that generated the sample.

### -param Sample

Address of a variable that receives a pointer to a <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure that contains the sample. When you have finished using the structure, you must pass the pointer to  <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory allocated for the sample.

### -param SampleSize [out, optional]

A pointer to a <b>SIZE_T</b> value that contains the size, in bytes,  of the <a href="/windows/desktop/SecBioMet/winbio-bir">WINBIO_BIR</a> structure returned in the <i>Sample</i> parameter.

### -param RejectDetail [out, optional]

A pointer to a <b>WINBIO_REJECT_DETAIL</b> value that contains additional information about the failure to capture a biometric sample. If the capture succeeded, this parameter is set to zero. The following values are defined for fingerprint capture:

<ul>
<li><b>WINBIO_FP_TOO_HIGH</b></li>
<li><b>WINBIO_FP_TOO_LOW</b></li>
<li><b>WINBIO_FP_TOO_LEFT</b></li>
<li><b>WINBIO_FP_TOO_RIGHT</b></li>
<li><b>WINBIO_FP_TOO_FAST</b></li>
<li><b>WINBIO_FP_TOO_SLOW</b></li>
<li><b>WINBIO_FP_POOR_QUALITY</b></li>
<li><b>WINBIO_FP_TOO_SKEWED</b></li>
<li><b>WINBIO_FP_TOO_SHORT</b></li>
<li><b>WINBIO_FP_MERGE_FAILURE</b></li>
</ul>

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
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed because a secure sensor is present in the sensor pool.

</td>
</tr>
</table>

## -remarks

To call this function successfully, you must open the session handle by specifying <b>WINBIO_FLAG_RAW</b> in the <i>Flags</i> parameter of the <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a> or <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a> functions. Currently, only applications running under the Administrators and Local System accounts have the necessary privileges.

Valid combinations of the <i>Purpose</i> and <i>Flags</i> parameters depend on the capabilities of the biometric unit being used. Consult the vendor's sensor  documentation to determine which combinations of valid <i>Purpose</i> and <i>Flags</i> values are supported and how they affect the captured data.
After you are finished using the sample, your application must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the memory allocated for it by the <b>WinBioCaptureSample</b> function.

To use <b>WinBioCaptureSample</b> synchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>. The function blocks until a sample has been captured or an error is encountered. Calls to <b>WinBioCaptureSample</b> using the system pool will block until the calling application has window focus and the user provides a sample to one of the sensors in the pool. If the sensor chosen by the user is already being used for an enrollment transaction, the function fails and returns <b>WINBIO_E_ENROLLMENT_IN_PROGRESS</b>.

To use <b>WinBioCaptureSample</b> asynchronously, call the function with a session handle created by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioasyncopensession">WinBioAsyncOpenSession</a>. The framework allocates a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. If the capture operation is successful, the framework returns information about the sample in a nested <b>CaptureSample</b> structure. If the operation is unsuccessful, the framework returns error information. The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_async_completion_callback">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="/windows/desktop/api/winbio/nf-winbio-winbiofree">WinBioFree</a> to release the <a href="/windows/desktop/api/winbio/ns-winbio-winbio_async_result">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.

<b>Windows 7:  </b>You can perform this operation asynchronously by using the <a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesamplewithcallback">WinBioCaptureSampleWithCallback</a> function. The function verifies the input arguments and returns immediately. If the input arguments are not valid, the function returns an error code. Otherwise, the framework starts the operation on another thread. When the asynchronous operation completes or encounters an error, the framework sends the results to  the <a href="/windows/desktop/api/winbio/nc-winbio-pwinbio_capture_callback">PWINBIO_CAPTURE_CALLBACK</a> function implemented by your application.


#### Examples

The following function calls <b>WinBioCaptureSample</b> to capture a biometric sample from a user. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT CaptureSample()
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    PWINBIO_BIR sample = NULL;
    SIZE_T sampleSize = 0;

    // Connect to the system pool. 
    hr = WinBioOpenSession( 
            WINBIO_TYPE_FINGERPRINT,    // Service provider
            WINBIO_POOL_SYSTEM,         // Pool type
            WINBIO_FLAG_RAW,            // Access: Capture raw data
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

    // Capture a biometric sample.
    wprintf_s(L"\n Calling WinBioCaptureSample - Swipe sensor...\n");
    hr = WinBioCaptureSample(
            sessionHandle,
            WINBIO_NO_PURPOSE_AVAILABLE,
            WINBIO_DATA_FLAG_RAW,
            &unitId,
            &sample,
            &sampleSize,
            &rejectDetail
            );
    if (FAILED(hr))
    {
        if (hr == WINBIO_E_BAD_CAPTURE)
        {
            wprintf_s(L"\n Bad capture; reason: %d\n", rejectDetail);
        }
        else
        {
            wprintf_s(L"\n WinBioCaptureSample failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;
    }

    wprintf_s(L"\n Swipe processed - Unit ID: %d\n", unitId);
    wprintf_s(L"\n Captured %d bytes.\n", sampleSize);


e_Exit:
    if (sample != NULL)
    {
        WinBioFree(sample);
        sample = NULL;
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

<a href="/windows/desktop/api/winbio/nf-winbio-winbiocapturesamplewithcallback">WinBioCaptureSampleWithCallback</a>