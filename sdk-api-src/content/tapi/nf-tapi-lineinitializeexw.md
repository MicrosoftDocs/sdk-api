---
UID: NF:tapi.lineInitializeExW
title: lineInitializeExW function (tapi.h)
description: The lineInitializeEx function initializes the application's use of TAPI for subsequent use of the line abstraction. (Unicode)
helpviewer_keywords: ["_tapi2_lineinitializeex", "lineInitializeEx", "lineInitializeEx function [TAPI 2.2]", "lineInitializeExW", "tapi/lineInitializeEx", "tapi/lineInitializeExW", "tapi2.lineinitializeex"]
old-location: tapi2\lineinitializeex.htm
tech.root: tapi3
ms.assetid: 18cd145d-e434-433a-ab10-91bf5b060c21
ms.date: 12/05/2018
ms.keywords: _tapi2_lineinitializeex, lineInitializeEx, lineInitializeEx function [TAPI 2.2], lineInitializeExA, lineInitializeExW, tapi/lineInitializeEx, tapi/lineInitializeExA, tapi/lineInitializeExW, tapi2.lineinitializeex
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: lineInitializeExW (Unicode) and lineInitializeExA (ANSI)
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
 - lineInitializeExW
 - tapi/lineInitializeExW
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
 - lineInitializeEx
 - lineInitializeExA
 - lineInitializeExW
---

# lineInitializeExW function


## -description

The 
<b>lineInitializeEx</b> function initializes the application's use of TAPI for subsequent use of the line abstraction. It registers the application's specified notification mechanism and returns the number of line devices available to the application. A line device is any device that provides an implementation for the line-prefixed functions in the Telephony API.

## -parameters

### -param lphLineApp

Pointer to a location that is filled with the application's usage handle for TAPI.

### -param hInstance

Instance handle of the client application or DLL. The application or DLL can pass <b>NULL</b> for this parameter, in which case TAPI uses the module handle of the root executable of the process (for purposes of identifying call handoff targets and media mode priorities).

### -param lpfnCallback

Address of a callback function that is invoked to determine status and events on the line device, addresses, or calls, when the application is using the "hidden window" method of event notification (for more information see 
<a href="/windows/desktop/api/tapi/nc-tapi-linecallback">lineCallbackFunc</a>). This parameter is ignored and should be set to <b>NULL</b> when the application chooses to use the "event handle" or "completion port" event notification mechanisms.

### -param lpszFriendlyAppName

Pointer to a <b>null</b>-terminated text string that contains only displayable characters. If this parameter is not <b>NULL</b>, it contains an application-supplied name for the application. This name is provided in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure to indicate, in a user-friendly way, which application originated, or originally accepted or answered the call. This information can be useful for call-logging purposes. If <i>lpszFriendlyAppName</i> is <b>NULL</b>, the application's module file name is used instead (as returned by the function 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea">GetModuleFileName</a>).

### -param lpdwNumDevs

Pointer to a <b>DWORD</b>-sized location. Upon successful completion of this request, this location is filled with the number of line devices available to the application.

### -param lpdwAPIVersion

Pointer to a <b>DWORD</b>-sized location. The application must initialize this <b>DWORD</b>, before calling this function, to the highest API version it is designed to support (for example, the same value it would pass into <i>dwAPIHighVersion</i> parameter of 
<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>). Artificially high values must not be used; the value must be accurately set. TAPI translates any newer messages or structures into values or formats supported by the application's version. Upon successful completion of this request, this location is filled with the highest API version supported by TAPI, thereby allowing the application to detect and adapt to having been installed on a system with a different version of TAPI.

### -param lpLineInitializeExParams

Pointer to a structure of type 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a> containing additional parameters used to establish the association between the application and TAPI (specifically, the application's selected event notification mechanism and associated parameters).

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPNAME, LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_INVALPOINTER, LINEERR_REINIT, LINEERR_NOMEM, LINEERR_INVALPARAM.

## -remarks

Applications must select one of three mechanisms by which TAPI notifies the application of telephony events: Hidden Window, Event Handle, or Completion Port.

The Hidden Window mechanism is selected by specifying LINEINITIALIZEEXOPTION_USEHIDDENWINDOW in the <b>dwOptions</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a> structure. In this mechanism (which is the only mechanism available to TAPI version 1.<i>x</i> applications), TAPI creates a window in the context of the application during the 
<b>lineInitializeEx</b> or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a> (for TAPI version 1.3 and 1.4 applications) function, and subclasses the window so that all messages posted to it are handled by a WNDPROC in TAPI itself. When TAPI has a message to deliver to the application, TAPI posts a message to the hidden window. When the message is received (which can happen only when the application calls the Windows 
<a href="/previous-versions/windows/desktop/fax/-mfax-faxaccountincomingarchive-getmessage-vb">GetMessage</a> function), Windows switches the process context to that of the application and invokes the WNDPROC in TAPI. TAPI then delivers the message to the application by calling the <i>lineCallbackProc</i>, a pointer to which the application provided as a parameter in its call to 
<b>lineInitializeEx</b> (or 
<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a>). This mechanism requires the application to have a message queue (which is not desirable for service processes) and to service that queue regularly to avoid delaying processing of telephony events. The hidden window is destroyed by TAPI during the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> function.

The Event Handle mechanism is selected by specifying LINEINITIALIZEEXOPTION_USEEVENT in the <b>dwOptions</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a> structure. In this mechanism, TAPI creates an event object on behalf of the application, and returns a handle to the object in the <b>hEvent</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a>. The application must not manipulate this event in any manner (for example, must not call 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>, 
<a href="/windows/desktop/api/synchapi/nf-synchapi-resetevent">ResetEvent</a>, 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>, and so on) or undefined behavior results; the application can only wait on this event using functions such as 
<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a> or 
<a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects">MsgWaitForMultipleObjects</a>. TAPI signals this event whenever a telephony event notification is pending for the application; the application must call 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetmessage">lineGetMessage</a> to fetch the contents of the message. The event is reset by TAPI when no events are pending. The event handle is closed and the event object destroyed by TAPI during the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a> function. The application is not required to wait on the event handle that is created; the application could choose instead to call 
<b>lineGetMessage</b> and have it block waiting for a message to be queued.

The Completion Port mechanism is selected by specifying LINEINITIALIZEEXOPTION_USECOMPLETION PORT in the <b>dwOptions</b> member in the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a> structure. In this mechanism, whenever a telephony event needs to be sent to the application, TAPI sends it using 
<a href="/windows/desktop/FileIO/postqueuedcompletionstatus">PostQueuedCompletionStatus</a> to the completion port that the application specified in the <b>hCompletionPort</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a>, tagged with the completion key that the application specified in the <b>dwCompletionKey</b> member in 
<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a>. The application must have previously created the completion port using 
<a href="/windows/desktop/FileIO/createiocompletionport">CreateIoCompletionPort</a>. The application retrieves events using 
<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>. Upon return from <b>GetQueuedCompletionStatus</b>, the application has the specified <b>dwCompletionKey</b> written to the <b>DWORD</b> pointed to by the <i>lpCompletionKey</i> parameter, and a pointer to a 
<a href="/windows/desktop/api/tapi/ns-tapi-linemessage">LINEMESSAGE</a> structure returned to the location pointed to by <i>lpOverlapped</i>. After the application has processed the event, it is the application's responsibility to call 
<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release the memory used to contain the 
<b>LINEMESSAGE</b> structure. Because the application created the completion port (thereby allowing it to be shared for other purposes), the application must close it; the application must not close the completion port until after calling 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>.

When a multithreaded application is using the Event Handle mechanism and more than one thread is waiting on the handle, or the Completion Port notification mechanism and more than one thread is waiting on the port, it is possible for telephony events to be processed out of sequence. This is not due to the sequence of delivery of events from TAPI, but would be caused by the time slicing of threads or the execution of threads on separate processors.

If LINEERR_REINIT is returned and TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then 
<b>lineInitializeEx</b> requests are rejected with this error until the last application shuts down its usage of the API (using 
<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>), at which time the new configuration becomes effective and applications are once again permitted to call 
<b>lineInitializeEx</b>.

If the LINEERR_INVALPARAM error value is returned, the specified <i>hInstance</i> parameter is invalid.

The application can refer to individual line devices by using line device identifiers that range from zero to <i>dwNumDevs</i> minus one. An application should not assume that these line devices are capable of any particular TAPI function without first querying their device capabilities by 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>.





> [!NOTE]
> The tapi.h header defines lineInitializeEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Tapi/basic-telephony-services-reference">Basic Telephony Services Reference</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineinitializeexparams">LINEINITIALIZEEXPARAMS</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemessage">LINEMESSAGE</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nc-tapi-linecallback">lineCallbackFunc</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetaddresscaps">lineGetAddressCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetmessage">lineGetMessage</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineinitialize">lineInitialize</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linenegotiateapiversion">lineNegotiateAPIVersion</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineshutdown">lineShutdown</a>
