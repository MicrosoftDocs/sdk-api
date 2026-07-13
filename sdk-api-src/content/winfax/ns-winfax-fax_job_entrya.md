---
UID: NS:winfax._FAX_JOB_ENTRYA
title: FAX_JOB_ENTRYA (winfax.h)
description: The FAX_JOB_ENTRY structure describes one fax job. (ANSI)
helpviewer_keywords: ["*PFAX_JOB_ENTRYA","DRT_EMAIL","DRT_INBOX","DRT_NONE","FAX_JOB_ENTRY","FAX_JOB_ENTRY structure [Fax Service]","FAX_JOB_ENTRYA","FAX_JOB_ENTRYW","FPS_ABORTING","FPS_ANSWERED","FPS_AVAILABLE","FPS_BAD_ADDRESS","FPS_BUSY","FPS_CALL_BLACKLISTED","FPS_CALL_DELAYED","FPS_COMPLETED","FPS_DIALING","FPS_DISCONNECTED","FPS_FATAL_ERROR","FPS_HANDLED","FPS_INITIALIZING","FPS_NOT_FAX_CALL","FPS_NO_ANSWER","FPS_NO_DIAL_TONE","FPS_OFFLINE","FPS_RECEIVING","FPS_RINGING","FPS_ROUTING","FPS_SENDING","FPS_UNAVAILABLE","JSA_DISCOUNT_PERIOD","JSA_NOW","JSA_SPECIFIC_TIME","JS_DELETING","JS_FAILED","JS_INPROGRESS","JS_NOLINE","JS_PAUSED","JS_PENDING","JS_RETRIES_EXCEEDED","JS_RETRYING","JT_FAIL_RECEIVE","JT_RECEIVE","JT_ROUTING","JT_SEND","JT_UNKNOWN","PFAX_JOB_ENTRY","PFAX_JOB_ENTRY structure pointer [Fax Service]","_mfax_fax_job_entry_str","fax._mfax_fax_job_entry_str","winfax/FAX_JOB_ENTRY","winfax/FAX_JOB_ENTRYA","winfax/FAX_JOB_ENTRYW","winfax/PFAX_JOB_ENTRY"]
old-location: fax\_mfax_fax_job_entry_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_09de.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_JOB_ENTRYA, DRT_EMAIL, DRT_INBOX, DRT_NONE, FAX_JOB_ENTRY, FAX_JOB_ENTRY structure [Fax Service], FAX_JOB_ENTRYA, FAX_JOB_ENTRYW, FPS_ABORTING, FPS_ANSWERED, FPS_AVAILABLE, FPS_BAD_ADDRESS, FPS_BUSY, FPS_CALL_BLACKLISTED, FPS_CALL_DELAYED, FPS_COMPLETED, FPS_DIALING, FPS_DISCONNECTED, FPS_FATAL_ERROR, FPS_HANDLED, FPS_INITIALIZING, FPS_NOT_FAX_CALL, FPS_NO_ANSWER, FPS_NO_DIAL_TONE, FPS_OFFLINE, FPS_RECEIVING, FPS_RINGING, FPS_ROUTING, FPS_SENDING, FPS_UNAVAILABLE, JSA_DISCOUNT_PERIOD, JSA_NOW, JSA_SPECIFIC_TIME, JS_DELETING, JS_FAILED, JS_INPROGRESS, JS_NOLINE, JS_PAUSED, JS_PENDING, JS_RETRIES_EXCEEDED, JS_RETRYING, JT_FAIL_RECEIVE, JT_RECEIVE, JT_ROUTING, JT_SEND, JT_UNKNOWN, PFAX_JOB_ENTRY, PFAX_JOB_ENTRY structure pointer [Fax Service], _mfax_fax_job_entry_str, fax._mfax_fax_job_entry_str, winfax/FAX_JOB_ENTRY, winfax/FAX_JOB_ENTRYA, winfax/FAX_JOB_ENTRYW, winfax/PFAX_JOB_ENTRY'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_JOB_ENTRYW (Unicode) and FAX_JOB_ENTRYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_JOB_ENTRYA, *PFAX_JOB_ENTRYA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_JOB_ENTRYA
 - winfax/_FAX_JOB_ENTRYA
 - PFAX_JOB_ENTRYA
 - winfax/PFAX_JOB_ENTRYA
 - FAX_JOB_ENTRYA
 - winfax/FAX_JOB_ENTRYA
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
 - FAX_JOB_ENTRY
 - FAX_JOB_ENTRYA
 - FAX_JOB_ENTRYW
---

# FAX_JOB_ENTRYA structure


## -description

The <b>FAX_JOB_ENTRY</b> structure describes one fax job. The structure includes data on the job type and status, recipient and sender identification, scheduling and delivery settings, and the page count. The <b>SizeOfStruct</b> and <b>RecipientNumber</b> members are required.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_JOB_ENTRY</b> structure. The calling application must set this member to <b>sizeof(FAX_JOB_ENTRY)</b> before it calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetjoba">FaxSetJob</a> function.

### -field JobId

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job of interest. This number must match the value the calling application passes in the JobId parameter to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetjoba">FaxSetJob</a> function.

### -field UserName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the user who submitted the fax job.

### -field JobType

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that specifies the type of the fax job of interest. This member can be one of the following job types.



#### JT_SEND

The job is an outgoing fax transmission.



#### JT_RECEIVE

The job is an incoming fax transmission.



#### JT_UNKNOWN

The job type is unknown. This value indicates that the fax server has not yet scheduled the job.



#### JT_ROUTING

The fax server tried to route the fax transmission, but routing failed. The fax server will attempt to route the job again.



#### JT_FAIL_RECEIVE

The fax server did not route the fax because it did not receive the entire transmission. The fax server saves the partial transmission in a temporary directory.

### -field QueueStatus

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a set of bit flags indicating the queue status of the fax job identified by the <b>JobId</b> member. This member can be one or more of the following values.



#### JS_PENDING

The fax job is in the queue and pending service.



#### JS_INPROGRESS

The fax job is in progress.



#### JS_DELETING

The fax server is deleting the fax job.



#### JS_FAILED

The fax job failed.



#### JS_PAUSED

The fax server paused the fax job.



#### JS_NOLINE

There is no line available to send the fax. The fax server will send the transmission when a line is available.



#### JS_RETRYING

The fax job failed. The fax server will attempt to retransmit the fax after a specified interval. For more information about global configuration settings, such as retransmission intervals, see <a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>.



#### JS_RETRIES_EXCEEDED

The fax server exceeded the maximum number of retransmission attempts allowed. The fax will not be sent. For more information about global configuration settings, such as the maximum number of retransmission attempts, see <a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>.

### -field Status

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a fax device status code or value. This value can be one of the following predefined device status codes.



#### FPS_DIALING

The device is dialing a fax number.



#### FPS_SENDING

The device is sending a fax document.



#### FPS_RECEIVING

The device is receiving a fax document.



#### FPS_COMPLETED

The device completed sending or receiving a fax transmission.



#### FPS_UNAVAILABLE

The device is not available because it is in use by another application.



#### FPS_BUSY

The device encountered a busy signal.



#### FPS_NO_ANSWER

The receiving device did not answer the call.



#### FPS_BAD_ADDRESS

The device dialed an invalid fax number.



#### FPS_NO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone.



#### FPS_DISCONNECTED

The fax call was disconnected by the sender or the caller.



#### FPS_FATAL_ERROR

The device has encountered a fatal protocol error.



#### FPS_NOT_FAX_CALL

The device received a call that was a data call or a voice call.



#### FPS_CALL_DELAYED

The device delayed a fax call because the sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.) 



#### FPS_CALL_BLACKLISTED

The device could not complete a call because the telephone number was blocked or reserved; emergency numbers such as 911 are blocked.



#### FPS_INITIALIZING

The device is initializing a call.



#### FPS_OFFLINE

The device is offline and unavailable.



#### FPS_RINGING

The device is ringing.



#### FPS_AVAILABLE

The device is available.



#### FPS_ABORTING

The device is aborting a fax job.



#### FPS_ROUTING

The device is routing a received fax document.



#### FPS_ANSWERED

The device answered a new call.



#### FPS_HANDLED

The fax service processed the outbound fax document; the fax service provider will transmit the document.

### -field Size

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that contains the size, in bytes, of the fax document to transmit. The size must not exceed 4 GB.

### -field PageCount

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the total number of pages in the fax transmission.

### -field RecipientNumber

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the fax number of the recipient of the fax transmission.

### -field RecipientName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the recipient of the fax transmission.

### -field Tsid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the transmitting station identifier. This identifier is usually a telephone number.

### -field SenderName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the sender who initiated the fax transmission.

### -field SenderCompany

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the company name of the sender who initiated the fax transmission.

### -field SenderDept

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the department name of the sender who initiated the fax transmission.

### -field BillingCode

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that indicates an application- or server-specific billing code that applies to the fax transmission. The fax server uses the string to generate an entry in the fax event log. Billing codes are optional.

### -field ScheduleAction

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates when to send the fax. This member can be one of the following predefined job scheduling actions.



#### JSA_NOW

Send the fax as soon as a device is available.



#### JSA_SPECIFIC_TIME

Send the fax at the time specified by the <b>ScheduleTime</b> member.



#### JSA_DISCOUNT_PERIOD

Send the fax during the discount rate period. Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a> function to retrieve the discount period for the fax server.

### -field ScheduleTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a></b>

If the <b>ScheduleAction</b> member is equal to the value <b>JSA_SPECIFIC_TIME</b>, specifies a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date and time to send the fax. The time specified must be expressed in UTC.

### -field DeliveryReportType

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the type of email delivery report (DR) or nondelivery report (NDR) that the fax server should generate. This member can be one of the following predefined delivery report types.



#### DRT_NONE

Do not send a DR or an NDR to the sender of the fax transmission.



#### DRT_EMAIL

Send the DR or NDR in an email message to the sender of the fax transmission (supported in Windows Server 2003 and later).



#### DRT_INBOX

Send the DR or NDR in email to the sender's local personal folder store (PST).

### -field DeliveryReportAddress

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string. If the <b>DeliveryReportType</b> member is equal to <b>DRT_EMAIL</b>, the string is the address to which the DR or NDR should be sent. If the <b>DeliveryReportType</b> member is equal to <b>DRT_NONE</b>, this member must be <b>NULL</b>.

### -field DocumentName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string to associate with the fax document. This is the user-friendly name that appears in the print spooler.

## -remarks

A fax client application passes the <b>FAX_JOB_ENTRY</b> structure in a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetjoba">FaxSetJob</a> function.

An application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a> function to enumerate all queued and active fax jobs on the fax server of interest. <b>FaxEnumJobs</b> returns an array of <b>FAX_JOB_ENTRY</b> structures. Each structure describes one fax job in detail.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-jobs">Managing Fax Jobs</a>.





> [!NOTE]
> The winfax.h header defines FAX_JOB_ENTRY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumjobsa">FaxEnumJobs</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetjoba">FaxSetJob</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>
