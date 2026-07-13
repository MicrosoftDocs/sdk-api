---
UID: NF:winbio.WinBioUnregisterEventMonitor
title: WinBioUnregisterEventMonitor function (winbio.h)
description: Cancels event notifications from the service provider associated with an open biometric session.
helpviewer_keywords: ["WinBioUnregisterEventMonitor","WinBioUnregisterEventMonitor function [Windows Biometric Framework API]","secbiomet.winbiounregistereventmonitor","winbio/WinBioUnregisterEventMonitor"]
old-location: secbiomet\winbiounregistereventmonitor.htm
tech.root: SecBioMet
ms.assetid: 41a018be-2c7e-4700-8447-4fd5f919e5ba
ms.date: 12/05/2018
ms.keywords: WinBioUnregisterEventMonitor, WinBioUnregisterEventMonitor function [Windows Biometric Framework API], secbiomet.winbiounregistereventmonitor, winbio/WinBioUnregisterEventMonitor
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
 - WinBioUnregisterEventMonitor
 - winbio/WinBioUnregisterEventMonitor
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
 - WinBioUnregisterEventMonitor
---

# WinBioUnregisterEventMonitor function


## -description

The <b>WinBioUnregisterEventMonitor</b> function cancels event notifications from the service provider associated with an open biometric session.

## -parameters

### -param SessionHandle [in]

A <b>WINBIO_SESSION_HANDLE</b> value that identifies the open biometric session. Open the session handle by calling <a href="/windows/desktop/api/winbio/nf-winbio-winbioopensession">WinBioOpenSession</a>.

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
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
</table>

## -remarks

Call the <a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a> function to begin receiving event notifications.

If an application registers a <b>WinBio</b> event monitor and leaves that monitor active during a sleep/wake cycle, systems that implement biometric pre-boot authentication (PBA)/single sign-on features may not always work. The problem is that the PBA biometric call is intercepted by the event monitor before the system's biometric credential provider has a chance to perform its first <a href="/windows/desktop/api/winbio/nf-winbio-winbioidentify">WinBioIdentify</a> operation. Apps that use the <b>WinBio</b> event monitoring feature should unregister their monitors before the system sleeps, and re-register them after system wakeup. For more information on handling events during power state changes, see  <a href="/windows/desktop/Power/about-power-management">About Power Management</a>.




#### Examples

The following function registers an event monitor by calling the 
<a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a> function and passing the address
of a callback routine. The callback, also included,  receives event notifications 
from the Windows biometric framework. The function also calls <b>WinBioUnregisterEventMonitor</b> before closing the biometric session. Link to the Winbio.lib static library and include the following header files:

<ul>
<li>Windows.h</li>
<li>Stdio.h</li>
<li>Conio.h</li>
<li>Winbio.h</li>
</ul>

```cpp
HRESULT RegisterSystemEventMonitor(BOOL bCancel)
{
    HRESULT hr = S_OK;
    WINBIO_SESSION_HANDLE sessionHandle = NULL;
    WINBIO_UNIT_ID unitId = 0;

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
        wprintf_s(L"\n WinBioOpenSession failed. hr = 0x%x\n", hr);
        goto e_Exit;
    }

    // Call the WinBioRegisterEventMonitor function.
    wprintf_s(L"\n Calling WinBioRegisterEventMonitor.\n");
    hr = WinBioRegisterEventMonitor(
            sessionHandle,              // Open session handle
            WINBIO_EVENT_FP_UNCLAIMED,  // Events to monitor
            EventMonitorCallback,       // Callback function
            NULL                        // Optional context.
            );
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioRegisterEventMonitor failed.");
        wprintf_s(L"hr = 0x%x\n", hr);
        goto e_Exit;
    }
    wprintf_s(L"\n Waiting for an event.\n");


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

    // Wait for an event to happen.
    //wprintf_s(L"\n Swipe the sensor to receive an event notice ");
    //wprintf_s(L"\n or press any key to stop waiting...\n");
    wprintf_s(L"\n Swipe the sensor one or more times ");
    wprintf_s(L"to generate events.");
    wprintf_s(L"\n When done, press a key to exit...\n");
    _getch();

    // Unregister the event monitor.
    wprintf_s(L"\n Calling WinBioUnregisterEventMonitor\n");
    hr = WinBioUnregisterEventMonitor( sessionHandle);
    if (FAILED(hr))
    {
        wprintf_s(L"\n WinBioUnregisterEventMonitor failed.");
        wprintf_s(L"hr = 0x%x\n", hr);
    }

e_Exit:

    if (sessionHandle != NULL)
    {
       wprintf_s(L"\n Closing the session.\n");

        hr = WinBioCloseSession(sessionHandle);
        if (FAILED(hr))
        {
            wprintf_s(L"\n WinBioCloseSession failed. hr = 0x%x\n", hr);
        }
        sessionHandle = NULL;
    }

    wprintf_s(L"\n Press any key to exit...");
    _getch();

    return hr;
}

//------------------------------------------------------------------------
// The following function is the callback for WinBioRegisterEventMonitor.
// The function filters any event notice from the biometric subsystem and 
// writes a result to the console window.
// 
VOID CALLBACK EventMonitorCallback(
    __in_opt PVOID EventCallbackContext,
    __in HRESULT OperationStatus,
    __in PWINBIO_EVENT Event
    )
{
    UNREFERENCED_PARAMETER(EventCallbackContext);

    wprintf_s(L"\n EventMonitorCallback executing.");

    // Failure.
    if (FAILED(OperationStatus))
    {
        wprintf_s(L"\n EventMonitorCallback failed. ");
        wprintf_s(L" OperationStatus = 0x%x\n", OperationStatus);
        goto e_Exit;
    }

    // An event notice was received.
    if (Event != NULL)
    {
        wprintf_s(L"\n MonitorEvent: ");
        switch (Event->Type)
        {
            case WINBIO_EVENT_FP_UNCLAIMED:
                wprintf_s(L"WINBIO_EVENT_FP_UNCLAIMED");
                wprintf_s(L"\n Unit ID: %d", 
                          Event->Parameters.Unclaimed.UnitId);
                wprintf_s(L"\n Reject detail: %d\n", 
                          Event->Parameters.Unclaimed.RejectDetail);
                break;

            case WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY:
                wprintf_s(L"WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY");
                wprintf_s(L"\n Unit ID: %d", 
                          Event->Parameters.UnclaimedIdentify.UnitId);
                wprintf_s(L"\n Reject detail: %d\n", 
                          Event->Parameters.UnclaimedIdentify.RejectDetail);
                break;

            case WINBIO_EVENT_ERROR:
                wprintf_s(L"WINBIO_EVENT_ERROR\n");
                break;

            default:
                wprintf_s(L"(0x%08x - Invalid type)\n", Event->Type);
                break;
        }
    }

e_Exit:

    if (Event != NULL)
    {
        //wprintf_s(L"\n Press any key to continue...\n");
        WinBioFree(Event);
        Event = NULL;
    }
}


```

## -see-also

<a href="/windows/desktop/api/winbio/nf-winbio-winbioregistereventmonitor">WinBioRegisterEventMonitor</a>