---
UID: NF:tapi.phoneInitializeExA
title: phoneInitializeExA function (tapi.h)
description: The phoneInitializeEx function initializes the application's use of TAPI for subsequent use of the phone abstraction. (ANSI)
helpviewer_keywords: ["phoneInitializeExA", "tapi/phoneInitializeExA"]
old-location: tapi2\phoneinitializeex.htm
tech.root: tapi3
ms.assetid: 362e37df-4b14-4651-8d23-b70613e354c8
ms.date: 12/05/2018
ms.keywords: _tapi2_phoneinitializeex, phoneInitializeEx, phoneInitializeEx function [TAPI 2.2], phoneInitializeExA, phoneInitializeExW, tapi/phoneInitializeEx, tapi/phoneInitializeExA, tapi/phoneInitializeExW, tapi2.phoneinitializeex
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: phoneInitializeExW (Unicode) and phoneInitializeExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phoneInitializeExA
 - tapi/phoneInitializeExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - phoneInitializeEx
 - phoneInitializeExA
 - phoneInitializeExW
---

# phoneInitializeExA function


## -description

The 
<b>phoneInitializeEx</b> function initializes the application's use of TAPI for subsequent use of the phone abstraction. It registers the application's specified notification mechanism and returns the number of phone devices available to the application. A phone device is any device that provides an implementation for the phone-prefixed functions in the Telephony API.

## -parameters

### -param lphPhoneApp

Pointer to a location that is filled with the application's usage handle for TAPI.

### -param hInstance

Instance handle of the client application or DLL. The application or DLL can pass <b>NULL</b> for this parameter, in which case TAPI uses the module handle of the root executable of the process.

### -param lpfnCallback

Address of a callback function that is invoked to determine status and events on the line device, addresses, or calls, when the application is using the "hidden window" method of event notification (for more information see 
<a href="/windows/desktop/api/tapi/nc-tapi-phonecallback">phoneCallbackFunc</a>). This parameter is ignored and should be set to <b>NULL</b> when the application chooses to use the "event handle" or "completion port" event notification mechanisms.

### -param lpszFriendlyAppName

Pointer to a <b>null</b>-terminated string that contains only displayable characters. If this parameter is not <b>NULL</b>, it contains an application-supplied name for the application. This name is provided in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a> structure to indicate, in a user-friendly way, which application has ownership of the phone device. If <i>lpszFriendlyAppName</i> is <b>NULL</b>, the application's module filename is used instead (as returned by the function 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea">GetModuleFileName</a>).

### -param lpdwNumDevs

Pointer to a <b>DWORD</b>. Upon successful completion of this request, this location is filled with the number of phone devices available to the application.

### -param lpdwAPIVersion

Pointer to a <b>DWORD</b>. The application must initialize this <b>DWORD</b>, before calling this function, to the highest API version it is designed to support (for example, the same value it would pass into <i>dwAPIHighVersion</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>). Artificially high values must not be used; the value must be accurately set. TAPI translates any newer messages or structures into values or formats supported by the application's version. Upon successful completion of this request, this location is filled with the highest API version supported by TAPI, thereby allowing the application to detect and adapt to having been installed on a system with an older version of TAPI.

### -param lpPhoneInitializeExParams

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a> containing additional parameters used to establish the association between the application and TAPI (specifically, the application's selected event notification mechanism and associated parameters).

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPNAME, PHONEERR_OPERATIONFAILED, PHONEERR_INIFILECORRUPT, PHONEERR_INVALPOINTER, PHONEERR_REINIT, PHONEERR_NOMEM, PHONEERR_INVALPARAM.

## -remarks

Applications must select one of three mechanisms by which TAPI notifies the application of telephony events: Hidden Window, Event Handle, or Completion Port.

<ul>
<li>The <b>Hidden Window</b> mechanism is selected by specifying PHONEINITIALIZEEXOPTION_USEHIDDENWINDOW in the <b>dwOptions</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a> structure. In this mechanism (which is the only mechanism available to TAPI version 1.<i>x</i> applications), TAPI creates a window in the context of the application during the 
<b>phoneInitializeEx</b> function, and subclasses the window so that all messages posted to it are handled by a WNDPROC in TAPI itself. When TAPI has a message to deliver to the application, TAPI posts a message to the hidden window. When the message is received (which can happen only when the application calls the Windows 
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> function), Windows switches the process context to that of the application and invokes the WNDPROC in TAPI. TAPI then delivers the message to the application by calling the 
<a href="/windows/desktop/api/tapi/nc-tapi-phonecallback">phoneCallbackFunc</a>, a pointer to which the application provided as a parameter in its call to 
<b>phoneInitializeEx</b> (or 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneinitialize">phoneInitialize</a>, for TAPI version 1.3 and 1.4 applications). This mechanism requires the application to have a message queue (which is not desirable for service processes) and to service that queue regularly to avoid delaying processing of telephony events. The hidden window is destroyed by TAPI during the 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a> function.</li>
<li>The <b>Event Handle</b> mechanism is selected by specifying PHONEINITIALIZEEXOPTION_USEEVENT in the <b>dwOptions</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a> structure. In this mechanism, TAPI creates an event object on behalf of the application, and returns a handle to the object in the <b>hEvent</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a>. The application must not manipulate this event in any manner (for example, must not call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>, 
<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a>, 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>, and so on) or undefined behavior results; the application can only wait on this event using functions such as 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>. TAPI signals this event whenever a telephony event notification is pending for the application; the application must call 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetmessage">phoneGetMessage</a> to fetch the contents of the message. The event is reset by TAPI when no events are pending. The event handle is closed and the event object destroyed by TAPI during the 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a> function. The application is not required to wait on the event handle that is created; the application could choose instead to call 
<b>phoneGetMessage</b> and have it block waiting for a message to be queued.</li>
<li>The <b>Completion Port</b> mechanism is selected by specifying PHONEINITIALIZEEXOPTION_USECOMPLETION PORT in the <b>dwOptions</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a> structure. In this mechanism, whenever a telephony event needs to be sent to the application, TAPI sends it to the application using 
<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a> to the completion port that the application specified in the <b>hCompletionPort</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a>, tagged with the completion key that the application specified in the <b>dwCompletionKey</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a>. The application must have previously created the completion port using 
<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>. The applications retrieves events using 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>. Upon return from <b>GetQueuedCompletionStatus</b>, the application has the specified <b>dwCompletionKey</b> written to the <b>DWORD</b> pointed to by the <i>lpCompletionKey</i> parameter, and a pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-phonemessage">PHONEMESSAGE</a> structure returned to the location pointed to by <i>lpOverlapped</i>. After the application has processed the event, the application must call 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the memory used to contain the 
<b>PHONEMESSAGE</b> structure. Because the application created the completion port (thereby allowing it to be shared for other purposes), the application must close it; the application must not close the completion port until after calling 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a>.</li>
</ul>
When a multithreaded application is using the Event Handle mechanism and more than one thread is waiting on the handle, or the Completion Port notification mechanism and more than one thread is waiting on the port, it is possible for telephony events to be processed out of sequence. This is not due to the sequence of delivery of events from TAPI, but would be caused by the time slicing of threads or the execution of threads on separate processors.

If PHONEERR_REINIT is returned and TAPI reinitialization has been requested (for example, as a result of adding or removing a telephony service provider), then 
<b>phoneInitializeEx</b> requests are rejected with this error until the last application shuts down its usage of the API (using 
<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a>). At that time, the new configuration becomes effective and applications are once again permitted to call 
<b>phoneInitializeEx</b>.

If the PHONEERR_INVALPARAM error value is returned, the specified <i>hInstance</i> parameter is invalid.

The application can refer to individual phone devices by using phone device identifiers that range from zero to <i>dwNumDevs</i> minus one. An application should not assume that these phone devices are capable of any particular TAPI function without first querying their device capabilities by 
<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>.





> [!NOTE]
> The tapi.h header defines phoneInitializeEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-phoneinitializeexparams">PHONEINITIALIZEEXPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonemessage">PHONEMESSAGE</a>



<a href="/windows/desktop/api/tapi/ns-tapi-phonestatus">PHONESTATUS</a>



<a href="/windows/desktop/Tapi/supplementary-phone-service-functions">Supplementary Phone Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nc-tapi-phonecallback">phoneCallbackFunc</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetdevcaps">phoneGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonegetmessage">phoneGetMessage</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phoneshutdown">phoneShutdown</a>
