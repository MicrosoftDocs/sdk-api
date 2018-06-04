---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FAX_JOB_ENTRYA structure


## -description


The <b>FAX_JOB_ENTRY</b> structure describes one fax job. The structure includes data on the job type and status, recipient and sender identification, scheduling and delivery settings, and the page count. The <b>SizeOfStruct</b> and <b>RecipientNumber</b> members are required.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_JOB_ENTRY</b> structure. The calling application must set this member to <b>sizeof(FAX_JOB_ENTRY)</b> before it calls the <a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a> function.


### -field JobId

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job of interest. This number must match the value the calling application passes in the JobId parameter to the <a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a> function.


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

The fax job failed. The fax server will attempt to retransmit the fax after a specified interval. For more information about global configuration settings, such as retransmission intervals, see <a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a>.



#### JS_RETRIES_EXCEEDED

The fax server exceeded the maximum number of retransmission attempts allowed. The fax will not be sent. For more information about global configuration settings, such as the maximum number of retransmission attempts, see <a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a>.


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

Send the fax during the discount rate period. Call the <a href="https://msdn.microsoft.com/c29f0eaf-39a5-45e2-afb9-010494552969">FaxGetConfiguration</a> function to retrieve the discount period for the fax server.


### -field ScheduleTime

Type: <b><a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a></b>

If the <b>ScheduleAction</b> member is equal to the value <b>JSA_SPECIFIC_TIME</b>, specifies a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date and time to send the fax. The time specified must be expressed in UTC.


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



A fax client application passes the <b>FAX_JOB_ENTRY</b> structure in a call to the <a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a> function.

An application can call the <a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a> function to enumerate all queued and active fax jobs on the fax server of interest. <b>FaxEnumJobs</b> returns an array of <b>FAX_JOB_ENTRY</b> structures. Each structure describes one fax job in detail.

For more information, see <a href="https://msdn.microsoft.com/7eb47777-cf5c-463d-bf19-5884c6fed04f">Managing Fax Jobs</a>.




## -see-also




<a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/be81e221-4aba-4c63-9640-337bee49fdb4">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/d32cbef5-e548-4f66-bac6-c718c688547d">FaxEnumJobs</a>



<a href="https://msdn.microsoft.com/f9068b1d-2cac-4128-b112-23febd846c15">FaxSetJob</a>



<a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a>
 

 

