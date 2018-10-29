---
UID: NF:tapi.lineInitializeExW
title: lineInitializeExW function
author: windows-sdk-content
description: The lineInitializeEx function initializes the application's use of TAPI for subsequent use of the line abstraction.
old-location: tapi2\lineinitializeex.htm
tech.root: Tapi
ms.assetid: 18cd145d-e434-433a-ab10-91bf5b060c21
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "_tapi2_lineinitializeex, lineInitializeEx, lineInitializeEx function [TAPI 2.2], lineInitializeExA, lineInitializeExW, tapi/lineInitializeEx, tapi/lineInitializeExA, tapi/lineInitializeExW, tapi2.lineinitializeex"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/449ecf4f-0b1b-449e-9eae-049770d41dbc">lineCallbackFunc</a>). This parameter is ignored and should be set to <b>NULL</b> when the application chooses to use the "event handle" or "completion port" event notification mechanisms.


### -param lpszFriendlyAppName

Pointer to a <b>null</b>-terminated text string that contains only displayable characters. If this parameter is not <b>NULL</b>, it contains an application-supplied name for the application. This name is provided in the 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure to indicate, in a user-friendly way, which application originated, or originally accepted or answered the call. This information can be useful for call-logging purposes. If <i>lpszFriendlyAppName</i> is <b>NULL</b>, the application's module file name is used instead (as returned by the function 
<a href="https://msdn.microsoft.com/f124c99f-8be1-4a9c-a84c-b1b323921f1a">GetModuleFileName</a>).


### -param lpdwNumDevs

Pointer to a <b>DWORD</b>-sized location. Upon successful completion of this request, this location is filled with the number of line devices available to the application.


### -param lpdwAPIVersion

Pointer to a <b>DWORD</b>-sized location. The application must initialize this <b>DWORD</b>, before calling this function, to the highest API version it is designed to support (for example, the same value it would pass into <i>dwAPIHighVersion</i> parameter of 
<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>). Artificially high values must not be used; the value must be accurately set. TAPI translates any newer messages or structures into values or formats supported by the application's version. Upon successful completion of this request, this location is filled with the highest API version supported by TAPI, thereby allowing the application to detect and adapt to having been installed on a system with a different version of TAPI.


### -param lpLineInitializeExParams

Pointer to a structure of type 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a> containing additional parameters used to establish the association between the application and TAPI (specifically, the application's selected event notification mechanism and associated parameters).


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALAPPNAME, LINEERR_OPERATIONFAILED, LINEERR_INIFILECORRUPT, LINEERR_INVALPOINTER, LINEERR_REINIT, LINEERR_NOMEM, LINEERR_INVALPARAM.




## -remarks



Applications must select one of three mechanisms by which TAPI notifies the application of telephony events: Hidden Window, Event Handle, or Completion Port.

The Hidden Window mechanism is selected by specifying LINEINITIALIZEEXOPTION_USEHIDDENWINDOW in the <b>dwOptions</b> member in the 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a> structure. In this mechanism (which is the only mechanism available to TAPI verson 1.<i>x</i> applications), TAPI creates a window in the context of the application during the 
<b>lineInitializeEx</b> or 
<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a> (for TAPI version 1.3 and 1.4 applications) function, and subclasses the window so that all messages posted to it are handled by a WNDPROC in TAPI itself. When TAPI has a message to deliver to the application, TAPI posts a message to the hidden window. When the message is received (which can happen only when the application calls the Windows 
<a href="https://msdn.microsoft.com/en-us/library/Aa359047(v=VS.85).aspx">GetMessage</a> function), Windows switches the process context to that of the application and invokes the WNDPROC in TAPI. TAPI then delivers the message to the application by calling the <i>lineCallbackProc</i>, a pointer to which the application provided as a parameter in its call to 
<b>lineInitializeEx</b> (or 
<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a>). This mechanism requires the application to have a message queue (which is not desirable for service processes) and to service that queue regularly to avoid delaying processing of telephony events. The hidden window is destroyed by TAPI during the 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a> function.

The Event Handle mechanism is selected by specifying LINEINITIALIZEEXOPTION_USEEVENT in the <b>dwOptions</b> member in the 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a> structure. In this mechanism, TAPI creates an event object on behalf of the application, and returns a handle to the object in the <b>hEvent</b> member in 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a>. The application must not manipulate this event in any manner (for example, must not call 
<a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a>, 
<a href="https://msdn.microsoft.com/bba7caab-d1ed-4261-aeca-49f847458f4c">ResetEvent</a>, 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>, and so on) or undefined behavior results; the application can only wait on this event using functions such as 
<a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a> or 
<a href="https://msdn.microsoft.com/0629f1b3-6805-43a7-9aeb-4f80939ec62c">MsgWaitForMultipleObjects</a>. TAPI signals this event whenever a telephony event notification is pending for the application; the application must call 
<a href="https://msdn.microsoft.com/ed6df53e-b01d-40bc-8676-b0f7e0eacfd1">lineGetMessage</a> to fetch the contents of the message. The event is reset by TAPI when no events are pending. The event handle is closed and the event object destroyed by TAPI during the 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a> function. The application is not required to wait on the event handle that is created; the application could choose instead to call 
<b>lineGetMessage</b> and have it block waiting for a message to be queued.

The Completion Port mechanism is selected by specifying LINEINITIALIZEEXOPTION_USECOMPLETION PORT in the <b>dwOptions</b> member in the 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a> structure. In this mechanism, whenever a telephony event needs to be sent to the application, TAPI sends it using 
<a href="https://msdn.microsoft.com/en-us/library/Aa365458(v=VS.85).aspx">PostQueuedCompletionStatus</a> to the completion port that the application specified in the <b>hCompletionPort</b> member in 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a>, tagged with the completion key that the application specified in the <b>dwCompletionKey</b> member in 
<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a>. The application must have previously created the completion port using 
<a href="https://msdn.microsoft.com/en-us/library/Aa363862(v=VS.85).aspx">CreateIoCompletionPort</a>. The application retrieves events using 
<a href="https://msdn.microsoft.com/en-us/library/Aa364986(v=VS.85).aspx">GetQueuedCompletionStatus</a>. Upon return from <b>GetQueuedCompletionStatus</b>, the application has the specified <b>dwCompletionKey</b> written to the <b>DWORD</b> pointed to by the <i>lpCompletionKey</i> parameter, and a pointer to a 
<a href="https://msdn.microsoft.com/1d184948-4ba2-4c8c-8771-d1aea6c4f565">LINEMESSAGE</a> structure returned to the location pointed to by <i>lpOverlapped</i>. After the application has processed the event, it is the application's responsibility to call 
<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release the memory used to contain the 
<b>LINEMESSAGE</b> structure. Because the application created the completion port (thereby allowing it to be shared for other purposes), the application must close it; the application must not close the completion port until after calling 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>.

When a multithreaded application is using the Event Handle mechanism and more than one thread is waiting on the handle, or the Completion Port notification mechanism and more than one thread is waiting on the port, it is possible for telephony events to be processed out of sequence. This is not due to the sequence of delivery of events from TAPI, but would be caused by the time slicing of threads or the execution of threads on separate processors.

If LINEERR_REINIT is returned and TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then 
<b>lineInitializeEx</b> requests are rejected with this error until the last application shuts down its usage of the API (using 
<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>), at which time the new configuration becomes effective and applications are once again permitted to call 
<b>lineInitializeEx</b>.

If the LINEERR_INVALPARAM error value is returned, the specified <i>hInstance</i> parameter is invalid.

The application can refer to individual line devices by using line device identifiers that range from zero to <i>dwNumDevs</i> minus one. An application should not assume that these line devices are capable of any particular TAPI function without first querying their device capabilities by 
<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a> and 
<a href="https://msdn.microsoft.com/08cdea8a-5b36-428c-b90f-8741ae5f3205">lineGetAddressCaps</a>.




## -see-also




<a href="https://msdn.microsoft.com/09d10789-bc36-47c7-b77d-8698ae75541a">Basic Telephony Services Reference</a>



<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/17fed282-6d08-4702-9ceb-9cbcc3737395">LINEINITIALIZEEXPARAMS</a>



<a href="https://msdn.microsoft.com/1d184948-4ba2-4c8c-8771-d1aea6c4f565">LINEMESSAGE</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/449ecf4f-0b1b-449e-9eae-049770d41dbc">lineCallbackFunc</a>



<a href="https://msdn.microsoft.com/08cdea8a-5b36-428c-b90f-8741ae5f3205">lineGetAddressCaps</a>



<a href="https://msdn.microsoft.com/c0900c5b-8791-4653-8bfc-d32e51d10c50">lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/ed6df53e-b01d-40bc-8676-b0f7e0eacfd1">lineGetMessage</a>



<a href="https://msdn.microsoft.com/4b406f19-be9b-4130-91a7-5fdfa56f7fc3">lineInitialize</a>



<a href="https://msdn.microsoft.com/71eb55de-281b-42a9-8d9b-7ded62cb006a">lineNegotiateAPIVersion</a>



<a href="https://msdn.microsoft.com/d512508a-fb6a-41ec-a80d-f625abfdd184">lineShutdown</a>
 

 

