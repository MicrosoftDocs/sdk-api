---
UID: NF:winbio.WinBioEnrollCommit
title: WinBioEnrollCommit function
author: windows-sdk-content
description: Finalizes a pending biometric template and saves it to the database associated with the biometric unit used for enrollment. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbioenrollcommit.htm
tech.root: SecBioMet
ms.assetid: ed9242e5-fee7-46ca-b42c-cda1b5dcdc78
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WinBioEnrollCommit, WinBioEnrollCommit function [Windows Biometric Framework API], secbiomet.winbioenrollcommit, winbio/WinBioEnrollCommit
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
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioEnrollCommit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WinBioEnrollCommit function


## -description


Finalizes a pending biometric template and saves it to the database associated with the biometric unit used for enrollment. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies an open biometric session.  Open a synchronous session handle by calling <a href="https://msdn.microsoft.com/e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf">WinBioOpenSession</a>. Open an asynchronous session handle by calling <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>.


### -param Identity [out, optional]

Pointer to a  <a href="https://msdn.microsoft.com/58a5f4ba-2f58-466c-90fd-9480c3c095db">WINBIO_IDENTITY</a> structure that receives the identifier (GUID or SID) of the template.


### -param IsNewTemplate [out, optional]

Pointer to a Boolean value that specifies whether the template being added to the database is new.


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
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
The pointers specified by the <i>Identity</i> and <i>IsNewTemplate</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DATABASE_FULL</b></dt>
</dl>
</td>
<td width="60%">
There is no space available in the database for the template.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINBIO_E_DUPLICATE_TEMPLATE</b></dt>
</dl>
</td>
<td width="60%">
The template matches one already saved in the database with a different identity or sub-factor (system pool only).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_LOCK_VIOLATION</b></b></dt>
</dl>
</td>
<td width="60%">
The biometric unit is in use and is locked.

</td>
</tr>
</table>
 




## -remarks



If the pending template is a duplicate of one that already exists in the database, the <i>Identity</i> parameter will point to the existing template and the value pointed to by the <i>IsNewTemplate</i> parameter will be <b>FALSE</b>.

If the <b>WinBioEnrollCommit</b> function succeeds, the following registry value is set to 0x01.


<pre xml:space="preserve"><b>HKEY_LOCAL_MACHINE</b>
   <b>System</b>
      <b>CurrentControlSet</b>
         <b>Services</b>
            <b>WbioSrvc</b>
               <b>Parameters</b>
                  <b>EnrollmentCommitted</b></pre>


<div class="alert"><b>Note</b>  This registry value is never deleted by the Windows Biometric Framework (WBF).</div>
<div> </div>
To use <b>WinBioEnrollCommit</b> synchronously, call the function with a session handle created by calling <a href="https://msdn.microsoft.com/e9a0bb5f-4bbd-4dc4-9cd8-c26f5e4f74cf">WinBioOpenSession</a>. The function blocks until the operation completes or an error is encountered.

To use <b>WinBioEnrollCommit</b> asynchronously, call the function with a session handle created by calling <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>. The framework allocates a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure  and uses it to return information about operation success or failure. If the operation is successful, the framework returns <b>WINBIO_IDENTITY</b> information and a flag indicating whether the template is new in a nested <b>EnrollCommit</b> structure. If the operation is unsuccessful, the framework returns error information. The <b>WINBIO_ASYNC_RESULT</b> structure is returned to the application callback or to the application message queue, depending on the value you set in the <i>NotificationMethod</i> parameter of the <b>WinBioAsyncOpenSession</b> function:

<ul>
<li>If you choose to receive completion notices by using a callback, you must implement a <a href="https://msdn.microsoft.com/550EA13D-18CE-4B73-9C9B-4D5C46C48A75">PWINBIO_ASYNC_COMPLETION_CALLBACK</a> function and set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_CALLBACK</b>.</li>
<li>If you choose to receive completion notices by using the application message queue, you must set the  <i>NotificationMethod</i> parameter to <b>WINBIO_ASYNC_NOTIFY_MESSAGE</b>. The framework returns a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> pointer to the <b>LPARAM</b> field of the window message.</li>
</ul>
To prevent memory leaks, you must call <a href="https://msdn.microsoft.com/b570fc6c-a08e-4485-a621-20f59bd63d40">WinBioFree</a> to release the <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure after you have finished using it.


#### Examples

The following function calls <b>WinBioEnrollCommit</b> to commit a biometric enrollment to system pool. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT EnrollSysPool(
                      BOOL discardEnrollment, 
                      WINBIO_BIOMETRIC_SUBTYPE subFactor)
{
    HRESULT hr = S_OK;
    WINBIO_IDENTITY identity = {0};
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;
    WINBIO_REJECT_DETAIL rejectDetail = 0;
    BOOLEAN isNewTemplate = TRUE;

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
        wprintf_s(L"\n WinBioOpenSession failed. ");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Locate a sensor.
    wprintf_s(L"\n Swipe your finger on the sensor...\n");
    hr = WinBioLocateSensor( sessionHandle, &unitId);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Begin the enrollment sequence. 
    wprintf_s(L"\n Starting enrollment sequence...\n");
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

    // Capture enrollment information by swiping the sensor with
    // the finger identified by the subFactor argument in the 
    // WinBioEnrollBegin function.
    for (int swipeCount = 1;; ++swipeCount)
    {
        wprintf_s(L"\n Swipe the sensor to capture %s sample.",
                 (swipeCount == 1)?L"the first":L"another");

        hr = WinBioEnrollCapture(
                sessionHandle,  // Handle to open biometric session
                &rejectDetail   // [out] Failure information
                );

        wprintf_s(L"\n Sample %d captured from unit number %d.", 
                  swipeCount, 
                  unitId);

        if (hr == WINBIO_I_MORE_DATA)
        {
            wprintf_s(L"\n    More data required.\n");
            continue;
        }
        if (FAILED(hr))
        {
            if (hr == WINBIO_E_BAD_CAPTURE)
            {
                wprintf_s(L"\n  Error: Bad capture; reason: %d", 
                          rejectDetail);
                continue;
            }
            else
            {
                wprintf_s(L"\n WinBioEnrollCapture failed. hr = 0x%x", hr);
                goto e_Exit;
            }
        }
        else
        {
            wprintf_s(L"\n    Template completed.\n");
            break;
        }
    }

    // Discard the enrollment if the appropriate flag is set.
    // Commit the enrollment if it is not discarded.
    if (discardEnrollment == TRUE)
    {
        wprintf_s(L"\n Discarding enrollment...\n\n");
        hr = WinBioEnrollDiscard( sessionHandle );
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioLocateSensor failed. hr = 0x%x\n", hr);
        }
        goto e_Exit;    
    }
    else
    {
        wprintf_s(L"\n Committing enrollment...\n");
        hr = WinBioEnrollCommit( 
                sessionHandle,      // Handle to open biometric session
                &identity,          // WINBIO_IDENTITY object for the user
                &isNewTemplate);    // Is this a new template

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

    wprintf_s(L" Press any key to continue...");
    _getch();

    return hr;
}


```





## -see-also




<a href="https://msdn.microsoft.com/ee706f2a-f544-4f53-b776-064d32e8acc8">WinBioEnrollBegin</a>



<a href="https://msdn.microsoft.com/a50f0c9f-7b9c-4d80-b8fc-8b83bc333578">WinBioEnrollCapture</a>



<a href="https://msdn.microsoft.com/809e7d2f-6b41-4afc-86c2-43b6611d6e48">WinBioEnrollCaptureWithCallback</a>



<a href="https://msdn.microsoft.com/0b029ace-1f5d-4cb2-9f09-51e5a11d2e5a">WinBioEnrollDiscard</a>
 

 

