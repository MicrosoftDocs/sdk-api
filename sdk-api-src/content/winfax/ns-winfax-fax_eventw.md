---
UID: NS:winfax._FAX_EVENTW
title: FAX_EVENTW (winfax.h)
description: The FAX_EVENT structure represents the contents of an I/O completion packet. The fax server sends the completion packet to notify a fax client application of an asynchronous fax server event. (Unicode)
helpviewer_keywords: ["*PFAX_EVENTW","FAX_EVENT","FAX_EVENT structure [Fax Service]","FAX_EVENTA","FAX_EVENTW","FEI_ABORTING","FEI_ANSWERED","FEI_BAD_ADDRESS","FEI_BUSY","FEI_CALL_BLACKLISTED","FEI_CALL_DELAYED","FEI_COMPLETED","FEI_DELETED","FEI_DIALING","FEI_DISCONNECTED","FEI_FATAL_ERROR","FEI_FAXSVC_ENDED","FEI_FAXSVC_STARTED","FEI_IDLE","FEI_JOB_QUEUED","FEI_MODEM_POWERED_OFF","FEI_MODEM_POWERED_ON","FEI_NEVENTS","FEI_NOT_FAX_CALL","FEI_NO_ANSWER","FEI_NO_DIAL_TONE","FEI_RECEIVING","FEI_RINGING","FEI_ROUTING","FEI_SENDING","PFAX_EVENT","PFAX_EVENT structure pointer [Fax Service]","_mfax_fax_event_str","fax._mfax_fax_event_str","winfax/FAX_EVENT","winfax/FAX_EVENTA","winfax/FAX_EVENTW","winfax/PFAX_EVENT"]
old-location: fax\_mfax_fax_event_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9bw2.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_EVENTW, FAX_EVENT, FAX_EVENT structure [Fax Service], FAX_EVENTA, FAX_EVENTW, FEI_ABORTING, FEI_ANSWERED, FEI_BAD_ADDRESS, FEI_BUSY, FEI_CALL_BLACKLISTED, FEI_CALL_DELAYED, FEI_COMPLETED, FEI_DELETED, FEI_DIALING, FEI_DISCONNECTED, FEI_FATAL_ERROR, FEI_FAXSVC_ENDED, FEI_FAXSVC_STARTED, FEI_IDLE, FEI_JOB_QUEUED, FEI_MODEM_POWERED_OFF, FEI_MODEM_POWERED_ON, FEI_NEVENTS, FEI_NOT_FAX_CALL, FEI_NO_ANSWER, FEI_NO_DIAL_TONE, FEI_RECEIVING, FEI_RINGING, FEI_ROUTING, FEI_SENDING, PFAX_EVENT, PFAX_EVENT structure pointer [Fax Service], _mfax_fax_event_str, fax._mfax_fax_event_str, winfax/FAX_EVENT, winfax/FAX_EVENTA, winfax/FAX_EVENTW, winfax/PFAX_EVENT'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_EVENTW (Unicode) and FAX_EVENTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_EVENTW, *PFAX_EVENTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_EVENTW
 - winfax/_FAX_EVENTW
 - PFAX_EVENTW
 - winfax/PFAX_EVENTW
 - FAX_EVENTW
 - winfax/FAX_EVENTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winfax.h
api_name:
 - FAX_EVENT
 - FAX_EVENTA
 - FAX_EVENTW
---

# FAX_EVENTW structure


## -description

The <b>FAX_EVENT</b> structure represents the contents of an I/O completion packet. The fax server sends the completion packet to notify a fax client application of an asynchronous fax server event.

To create a fax event queue, the fax client application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxinitializeeventqueue">FaxInitializeEventQueue</a> function. The queue enables the application to receive notifications of asynchronous events from the fax server.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_EVENT</b> structure. The fax server sets this member to <b>sizeof(FAX_EVENT)</b>.

### -field TimeStamp

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

Specifies a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time at which the fax server generated the event.

### -field DeviceId

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the permanent line identifier for the fax device of interest.

### -field EventId

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that identifies the current asynchronous event that occurred within the fax server. The following table lists the possible events and their meanings.



#### FEI_DIALING

The sending device is dialing a fax number. 



#### FEI_SENDING

The sending device is transmitting a page of fax data. 



#### FEI_RECEIVING

The receiving device is receiving a page of fax data. 



#### FEI_COMPLETED

The device has completed a fax transmission call. 



#### FEI_BUSY

The sending device has encountered a busy signal. 



#### FEI_NO_ANSWER

The receiving device does not answer. 



#### FEI_BAD_ADDRESS

The sending device cannot complete the call because the fax number is invalid. 



#### FEI_NO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone. 



#### FEI_DISCONNECTED

The device cannot complete the call because a fax device was disconnected, or because the fax call itself was disconnected. 



#### FEI_FATAL_ERROR

The device encountered a fatal protocol error. 



#### FEI_NOT_FAX_CALL

The modem device received a data call or a voice call. 



#### FEI_CALL_DELAYED

The sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.) 



#### FEI_CALL_BLACKLISTED

The device cannot complete the call because the telephone number is blocked or reserved; numbers such as 911 are blocked. 



#### FEI_RINGING

The receiving device is ringing. 



#### FEI_ABORTING

The device is aborting a fax job. 



#### FEI_ROUTING

The receiving device is routing a received fax document. 



#### FEI_MODEM_POWERED_ON

The modem device was turned on. 



#### FEI_MODEM_POWERED_OFF

The modem device was turned off. 



#### FEI_IDLE

The device is idle. 



#### FEI_FAXSVC_ENDED

The fax service has terminated. For more information, see the following Remarks section.



#### FEI_ANSWERED

The receiving device answered a new call. 



#### FEI_FAXSVC_STARTED

The fax service has started. For more information, see the following Remarks section.



#### FEI_JOB_QUEUED

The fax job has been queued. 



#### FEI_DELETED

The fax job has been processed. The job identifier for the job is no longer valid.



#### FEI_NEVENTS

The total number of fax events received. For more information, see the following Remarks section.

### -field JobId

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job of interest. If this member is equal to the value 0xffffffff, it indicates an inactive fax job. Note that this number is not a print spooler identification number. 


##### - EventId.FEI_ABORTING

The device is aborting a fax job. 


##### - EventId.FEI_ANSWERED

The receiving device answered a new call. 


##### - EventId.FEI_BAD_ADDRESS

The sending device cannot complete the call because the fax number is invalid. 


##### - EventId.FEI_BUSY

The sending device has encountered a busy signal. 


##### - EventId.FEI_CALL_BLACKLISTED

The device cannot complete the call because the telephone number is blocked or reserved; numbers such as 911 are blocked. 


##### - EventId.FEI_CALL_DELAYED

The sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.) 


##### - EventId.FEI_COMPLETED

The device has completed a fax transmission call. 


##### - EventId.FEI_DELETED

The fax job has been processed. The job identifier for the job is no longer valid.


##### - EventId.FEI_DIALING

The sending device is dialing a fax number. 


##### - EventId.FEI_DISCONNECTED

The device cannot complete the call because a fax device was disconnected, or because the fax call itself was disconnected. 


##### - EventId.FEI_FATAL_ERROR

The device encountered a fatal protocol error. 


##### - EventId.FEI_FAXSVC_ENDED

The fax service has terminated. For more information, see the following Remarks section.


##### - EventId.FEI_FAXSVC_STARTED

The fax service has started. For more information, see the following Remarks section.


##### - EventId.FEI_IDLE

The device is idle. 


##### - EventId.FEI_JOB_QUEUED

The fax job has been queued. 


##### - EventId.FEI_MODEM_POWERED_OFF

The modem device was turned off. 


##### - EventId.FEI_MODEM_POWERED_ON

The modem device was turned on. 


##### - EventId.FEI_NEVENTS

The total number of fax events received. For more information, see the following Remarks section. 


##### - EventId.FEI_NOT_FAX_CALL

The modem device received a data call or a voice call. 


##### - EventId.FEI_NO_ANSWER

The receiving device does not answer. 


##### - EventId.FEI_NO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone. 


##### - EventId.FEI_RECEIVING

The receiving device is receiving a page of fax data. 


##### - EventId.FEI_RINGING

The receiving device is ringing. 


##### - EventId.FEI_ROUTING

The receiving device is routing a received fax document. 


##### - EventId.FEI_SENDING

The sending device is transmitting a page of fax data.

## -remarks

After a fax client application receives the <b>FEI_FAXSVC_ENDED</b> message from the fax service, it will no longer receive fax events. To resume receiving fax events, the application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxinitializeeventqueue">FaxInitializeEventQueue</a> function again when the fax service restarts. The application can determine if the fax service is running by using the service control manager.

If the application receives events using notification messages, it can use the <b>FEI_NEVENTS</b> event. If the message is between the application's base window message and the base window message + <b>FEI_NEVENTS</b>, then the application can process the message as a fax window message. An application specifies the base window message using the <i>MessageStart</i> parameter to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxinitializeeventqueue">FaxInitializeEventQueue</a> function; the base window message must be greater than the <a href="/windows/desktop/winmsg/wm-user">WM_USER</a> message. For more information, see <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxclose">FaxClose</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-enabling-an-application-to-receive-notifications-of-fax-events">Enabling an Application to Receive Notifications of Fax Events</a>.





> [!NOTE]
> The winfax.h header defines FAX_EVENT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxclose">FaxClose</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxinitializeeventqueue">FaxInitializeEventQueue</a>
