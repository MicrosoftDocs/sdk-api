---
UID: NC:winbio.PWINBIO_CAPTURE_CALLBACK
title: PWINBIO_CAPTURE_CALLBACK
author: windows-sdk-content
description: Returns results from the asynchronous WinBioCaptureSampleWithCallback function.
old-location: secbiomet\pwinbio_capture_callback.htm
old-project: SecBioMet
ms.assetid: 7B517246-410C-49B6-9DEE-30E066D8F5C6
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: PWINBIO_CAPTURE_CALLBACK, PWINBIO_CAPTURE_CALLBACK function, PWINBIO_CAPTURE_CALLBACK function pointer [Windows Biometric Framework API], secbiomet.pwinbio_capture_callback, winbio/PWINBIO_CAPTURE_CALLBACK
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
 - PWINBIO_CAPTURE_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PWINBIO_CAPTURE_CALLBACK callback function


## -description


Called by the Windows Biometric Framework to return results from the   asynchronous <a href="https://msdn.microsoft.com/a99296c8-89da-4b2c-9a1b-fc10700ad48d">WinBioCaptureSampleWithCallback</a> function. The client application must implement this function.


<div class="alert"><b>Important</b>  We recommend that, beginning with Windows 8, you no longer use the  <b>PWINBIO_CAPTURE_CALLBACK</b>/<b>WinBioCaptureSampleWithCallback</b> combination. Instead, do the following:<ul>
<li>Implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function to receive notice when the operation completes.</li>
<li>Call the <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> function. Pass the address of your callback in the <i>CallbackRoutine</i> parameter. Pass  <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b> in the <i>NotificationMethod</i> parameter. Retrieve an asynchronous session handle.</li>
<li>Use the asynchronous session handle to call <a href="https://msdn.microsoft.com/365dcefb-3382-4b62-b47d-919e2d3f56f1">WinBioCaptureSample</a>. When the operation finishes, the Windows Biometric Framework will allocate and initialize a  <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure with the results and invoke your callback with a pointer to the results structure.</li>
<li>Call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> from your callback implementation to release the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.</li>
</ul>
</div>
<div> </div>



## -parameters




### -param CaptureCallbackContext [in, optional]

Pointer to a buffer defined by the application and passed to the <i>CaptureCallbackContext</i> parameter of the <a href="https://msdn.microsoft.com/a99296c8-89da-4b2c-9a1b-fc10700ad48d">WinBioCaptureSampleWithCallback</a> function. The buffer is not modified by the framework or the biometric unit. Your application can use the data to help it determine what actions to perform or to maintain additional information about the biometric capture.


### -param OperationStatus [in]

Error code returned by the capture operation.


### -param UnitId [in]

Biometric unit ID number.


### -param Sample [in]

Pointer to the sample data.


### -param SampleSize [in]

Size, in bytes, of the sample data pointed to by the <i>Sample</i> parameter.


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

The following code example captures a sample asynchronously by calling <a href="https://msdn.microsoft.com/a99296c8-89da-4b2c-9a1b-fc10700ad48d">WinBioCaptureSampleWithCallback</a> and passing a pointer to a custom callback function, CaptureSampleCallback. Link to the Winbio.lib static library and include the following header files:

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
<pre>HRESULT CaptureSampleWithCallback(BOOL bCancel)
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
            &amp;sessionHandle              // [out] Session handle
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

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/b1ae4e65-9e53-42dd-99ba-1910b72688dd">WINBIO_REJECT_DETAIL Constants</a>



<a href="https://msdn.microsoft.com/a99296c8-89da-4b2c-9a1b-fc10700ad48d">WinBioCaptureSampleWithCallback</a>
 

 

