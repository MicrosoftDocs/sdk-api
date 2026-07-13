---
UID: NS:winfax._FAX_DEVICE_STATUSA
title: FAX_DEVICE_STATUSA (winfax.h)
description: The FAX_DEVICE_STATUS structure contains information about the current status of a fax device. (ANSI)
helpviewer_keywords: ["*PFAX_DEVICE_STATUSA","FAX_DEVICE_STATUS","FAX_DEVICE_STATUS structure [Fax Service]","FAX_DEVICE_STATUSA","FAX_DEVICE_STATUSW","FPS_ABORTING","FPS_ANSWERED","FPS_AVAILABLE","FPS_BAD_ADDRESS","FPS_BUSY","FPS_CALL_BLACKLISTED","FPS_CALL_DELAYED","FPS_COMPLETED","FPS_DIALING","FPS_DISCONNECTED","FPS_FATAL_ERROR","FPS_HANDLED","FPS_INITIALIZING","FPS_NOT_FAX_CALL","FPS_NO_ANSWER","FPS_NO_DIAL_TONE","FPS_OFFLINE","FPS_RECEIVING","FPS_RINGING","FPS_ROUTING","FPS_SENDING","FPS_UNAVAILABLE","JT_RECEIVE","JT_SEND","JT_UNKNOWN","PFAX_DEVICE_STATUS","PFAX_DEVICE_STATUS structure pointer [Fax Service]","_mfax_fax_device_status_str","fax._mfax_fax_device_status_str","winfax/FAX_DEVICE_STATUS","winfax/FAX_DEVICE_STATUSA","winfax/FAX_DEVICE_STATUSW","winfax/PFAX_DEVICE_STATUS"]
old-location: fax\_mfax_fax_device_status_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6vle.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_DEVICE_STATUSA, FAX_DEVICE_STATUS, FAX_DEVICE_STATUS structure [Fax Service], FAX_DEVICE_STATUSA, FAX_DEVICE_STATUSW, FPS_ABORTING, FPS_ANSWERED, FPS_AVAILABLE, FPS_BAD_ADDRESS, FPS_BUSY, FPS_CALL_BLACKLISTED, FPS_CALL_DELAYED, FPS_COMPLETED, FPS_DIALING, FPS_DISCONNECTED, FPS_FATAL_ERROR, FPS_HANDLED, FPS_INITIALIZING, FPS_NOT_FAX_CALL, FPS_NO_ANSWER, FPS_NO_DIAL_TONE, FPS_OFFLINE, FPS_RECEIVING, FPS_RINGING, FPS_ROUTING, FPS_SENDING, FPS_UNAVAILABLE, JT_RECEIVE, JT_SEND, JT_UNKNOWN, PFAX_DEVICE_STATUS, PFAX_DEVICE_STATUS structure pointer [Fax Service], _mfax_fax_device_status_str, fax._mfax_fax_device_status_str, winfax/FAX_DEVICE_STATUS, winfax/FAX_DEVICE_STATUSA, winfax/FAX_DEVICE_STATUSW, winfax/PFAX_DEVICE_STATUS'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_DEVICE_STATUSW (Unicode) and FAX_DEVICE_STATUSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_DEVICE_STATUSA, *PFAX_DEVICE_STATUSA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_DEVICE_STATUSA
 - winfax/_FAX_DEVICE_STATUSA
 - PFAX_DEVICE_STATUSA
 - winfax/PFAX_DEVICE_STATUSA
 - FAX_DEVICE_STATUSA
 - winfax/FAX_DEVICE_STATUSA
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
 - FAX_DEVICE_STATUS
 - FAX_DEVICE_STATUSA
 - FAX_DEVICE_STATUSW
---

# FAX_DEVICE_STATUSA structure


## -description

The <b>FAX_DEVICE_STATUS</b> structure contains information about the current status of a fax device. In addition to the status, the structure also includes data on whether the device is currently sending or receiving a fax transmission, device and station identifiers, sender and recipient names, and routing information.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_DEVICE_STATUS</b> structure. The fax service sets this member to <b>sizeof(FAX_DEVICE_STATUS)</b>.

### -field CallerId

Type: <b>LPCTSTR</b>

If the <b>JobType</b> member is equal to the <b>JT_RECEIVE</b> job type, <b>CallerId</b> is a pointer to a null-terminated character string that identifies the calling device that sent the active fax document. This string can include the telephone number of the calling device.

### -field Csid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the called station identifier of the device.

### -field CurrentPage

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the number of the page in the fax transmission that the fax device is currently sending or receiving. The page count is relative to one.

### -field DeviceId

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the permanent line identifier for the fax device of interest.

### -field DeviceName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the fax device of interest.

### -field DocumentName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string to associate with the fax document that the device is currently sending or receiving. This is the user-friendly name that appears in the print spooler.

### -field JobType

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that identifies the type of fax job that is currently active on the device. This member can be one of the following job types.



#### JT_SEND

The fax device is sending a fax document.



#### JT_RECEIVE

The fax device is receiving a fax document.



#### JT_UNKNOWN

The fax device is in an unknown or idle state.

### -field PhoneNumber

Type: <b>LPCTSTR</b>

If the <b>JobType</b> member is equal to the <b>JT_SEND</b> job type, <b>PhoneNumber</b> is a pointer to a constant null-terminated character string that is the fax number dialed for the outgoing fax transmission.

### -field RoutingString

Type: <b>LPCTSTR</b>

If the <b>JobType</b> member is equal to the <b>JT_RECEIVE</b> job type, <b>RoutingString</b> is a pointer to a constant null-terminated character string that specifies the routing string for an incoming fax. The string must be of the form: 

                    

<code>Canonical-Phone-Number[|Additional-Routing-Info]</code>

where <code>Canonical-Phone-Number</code> is defined in the <a href="/windows/desktop/Tapi/address-ovr">Address</a> topic of the TAPI documentation (see the Canonical Address subheading); and <code>Additional-Routing-Info</code> is the <i>subaddress</i> of a Canonical Address, and uses the subaddress format.

### -field SenderName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the sender who initiated the fax transmission.

### -field RecipientName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the recipient of the fax transmission.

### -field Size

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the size, in bytes, of the active fax document.

### -field StartTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

Specifies a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the starting time of the current fax job expressed in UTC.

### -field Status

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is a fax device status code or value. This member can be one of the predefined device status codes shown following.



#### FPS_DIALING

The device is dialing a fax number.



#### FPS_SENDING

The device is sending a fax document.



#### FPS_RECEIVING

The device is receiving a fax document.



#### FPS_COMPLETED

The device has completed sending or receiving a fax transmission.



#### FPS_UNAVAILABLE

The device is not available because it is in use by another application.



#### FPS_BUSY

The device has encountered a busy signal.



#### FPS_NO_ANSWER

The receiving device did not answer the call.



#### FPS_BAD_ADDRESS

The device dialed an invalid fax number.



#### FPS_NO_DIAL_TONE

The sending device cannot complete the call because it does not detect a dial tone.



#### FPS_DISCONNECTED

The fax call was disconnected by the sender or the caller.



#### FPS_FATAL_ERROR

The device encountered a fatal protocol error.



#### FPS_NOT_FAX_CALL

The device has received a data call or a voice call.



#### FPS_CALL_DELAYED

The device delayed a fax call because the sending device received a busy signal multiple times. The device cannot retry the call because dialing restrictions exist. (Some countries/regions restrict the number of retry attempts when a number is busy.) 



#### FPS_CALL_BLACKLISTED

The device could not complete a call because the telephone number was blocked or reserved; numbers such as 911 are blocked.



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

### -field StatusString

Type: <b>LPCTSTR</b>

This member must be <b>NULL</b>.

### -field SubmittedTime

Type: <b><a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a></b>

Specifies a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the time the client submitted the fax document for transmission to the fax job queue. The time is expressed in UTC.

### -field TotalPages

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the total number of pages in the fax transmission.

### -field Tsid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the transmitting station identifier (TSID). This identifier is usually a telephone number.

### -field UserName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the user who submitted the active fax job.

## -remarks

The fax client application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetdevicestatusa">FaxGetDeviceStatus</a> function to retrieve status information for the fax device of interest. The function returns the information in a <b>FAX_DEVICE_STATUS</b> structure.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-device-management">Fax Device Management</a>. For information about the status information a fax service provider supplies for an active fax operation, see the <a href="/windows/desktop/api/faxdev/ns-faxdev-fax_dev_status">FAX_DEV_STATUS</a> topic.





> [!NOTE]
> The winfax.h header defines FAX_DEVICE_STATUS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetdevicestatusa">FaxGetDeviceStatus</a>
